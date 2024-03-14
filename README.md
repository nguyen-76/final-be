- Background
  - Holostagram is a instagram similar social platform that allows people to join by creating accounts. Each User should provide a name, an email, and a password to create an account.
  - The email address should not link to any account in the system. After joining holostagram, users can update their profile with Avatar, post picture and comment on other people picture
  - Users can send follow request to other people. Users can accept or decline a follow request. After accepting a follow request, user can see what other people post on their timeline
- Authentication
  - As a user, I can see a list of other users so that I can send, accept or decline follow requests.
  - As a user, I can see my current profile info.
  - As a user, I can see a specific user's profile given a username
  - As a user, I can update my profile with Avatar, biography.
- Posts
  - As a user, I can see a timeline of post
  - As a user, I can create a new post with a caption and an image.
  - As a user, I can delete my posts.
- Comments
  - As a user, I can see a list of comments on a post.
  - As a user, I can write comments on a post.
  - As a user, I can update my comments.
  - As a user, I can delete my comments.
- Reactions
  - As a user, I can react heart or unheart to a post or a comment.
- Friends
  - As a user, I can send a friend request to another user who is not my friend.
  - As a user, I can see a list of friend requests I have received.
  - As a user, I can see a list of my friends.
  - As a user, I can accept or decline a friend request.
  - As a user, I can cancel a friend request I sent.
  - As a user, I can unfriend a user in my friend list.
- API endpoints

- Auth APIs
/**
* @route POST /auth/login
* @description Log in with username and password
* @body {email, passsword}
* @access Public
*/

- Friend APIS
 /**
* @route GET /friends/requests/incoming
* @description Get the list of received pending requests
* @access Login required
*/

 /**
* @route GET /friends/requests/outgoing
* @description Get the list of sent pending requests
* @access Login required
*/

  /**
* @route GET /friends/
* @description Get the list of friends
* @access Login required
*/

  /**
* @route POST /friends/requests
* @description Send a friend request
* @body {to : User ID}
* @access Login required
*/

  /**
* @route PUT /friends/requests/:userId
* @description Accept/Reject a received pending requests
* @body {status : 'accepted' or 'declined'}
* @access Login required
  */

  /**
* @route DELETE /friends/requests/:userId
* @description cancel a friend request
* @access Login required
  */

  /**
* @route DELETE /friends/:userId
* @description remove a friend
* @access Login required
  */

- User APIs
  /**
* @route GET /users/page=1?&limit=10
* @description Get user with pagination
* @body
* @access Login required
  */

  /**
* @route GET /users/me
* @description Get current user info
* @body
* @access Login required
  */

  /**
* @route GET /users/:id
* @description Get user profile
* @body
* @access Login required
  */

  /**
* @route POST /users
* @description Register new user
* @body {name, email, password}
* @access Public
  */

  /**
* @route PUT /users/:id
* @description Update user profile
* @body {name, avatar, description, password}
* @access Login required
  */
  
- Post APIs

  /**
* @route GET /posts/:id/comments
* @description Get comments of a post
* @access Login required
  */
  
  /**
* @route GET /posts/:id
* @description Get a single post
* @access Login required
  */

  /**
* @route POST /posts
* @description Create a new post
* @body {content, image}
* @access Login reuqired
  */

  /**
* @route PUT /posts/user/userId? page=1&limit=10
* @description Get all posts a user can see with pagination
* @access Login required
  */

  /**
* @route PUT /posts/:id
* @description Update a post
* @body {content, image}
* @access Login required
  */

  /**
* @route DELETE /posts/:id
* @description Delete a post
* @access Login required
  */

- Comment APIs
  <details>
  /**
* @route GET /comments/:id
* @description Get details of a comment
* @access Login required
  */

  /**
* @route POST /comments
* @description Create a new comment
* @body {content, postId}
* @access Login required
  */

  /**
* @route PUT /comment:id
* @description Update a comment
* @access Login required
  */

  /**
* @route DELETE comments/:id
* @description Delete a comment
* @access Login required
  */

  /**
* @route DELETE /comments/:id
* @description Delete a comment
* @access Login required
  */

- Reaction APIs
  /**
* @route /users
* @description Like or unlike post
* @access Login required
  */

  /**
* @route
* @description
* @body
* @access Login required
  */
