 
API : https://beztbetz.com/blog/wp-json/wp/v2/post

Authorization : Basic Auth <br/>
Username : <username> <br/>
Password : <password> <br/>
# Posts
<section>
    <h2>List Of Categories</h2>
    <div class="secondary">
        <table class="arguments">
        <tr>
         <td><code>ID</code><br /></td>
         <td><p>Unique identifier for the Categories.</p></td>
        </tr>
        <tr>
         <td>1<br /></td>
         <td><p>Uncategorized</p></td>
        </tr>
        <tr>
         <td><code>2</code><br /></td>
         <td><p>Betting News</p></td>
        </tr>
        <tr>
         <td>3<br /></td>
         <td><p>Betting Tips</p></td>
        </tr>
        <tr>
         <td>4<br /></td>
         <td><p>Bookmakers News</p></td>
        </tr>
        <tr>
         <td>5<br /></td>
         <td><p>Boxing News</p></td>
        </tr>
        <tr>
         <td>6<br /></td>
         <td><p>Football News</p></td>
        </tr>
        </table>
    </div>
</section>

<section>
    <h2>List Of Tags</h2>
    <div class="secondary">
        <table class="arguments">
        <tr>
         <td><code>ID</code><br /></td>
         <td><p>Unique identifier for the Tags.</p></td>
        </tr>
        <tr>
         <td>7<br /></td>
         <td><p>Betting</p></td>
        </tr>
        <tr>
         <td><code>8</code><br /></td>
         <td><p>Gambling</p></td>
        </tr>
        <tr>
         <td>9<br /></td>
         <td><p>Game</p></td>
        </tr>
        <tr>
         <td>10<br /></td>
         <td><p>Prediction</p></td>
        </tr>
        <tr>
         <td>11<br /></td>
         <td><p>Sport</p></td>
        </tr>
<!--         <tr>
         <td>6<br /></td>
         <td><p>Football News</p></td>
        </tr> -->
        </table>
    </div>
</section>

<div>
   <section class="route">
      <div class="primary">
         <h2>List Posts</h2>
         <p>Query this endpoint to retrieve a collection of posts. The response you receive can be controlled and filtered using the URL query parameters below.</p>
         <h3>Definition</h3>
         <code>GET https://beztbetz.com/blog/wp-json/wp/v2/posts</code>
         <h3>Example Request</h3>
         <code>import requests
url = "https://beztbetz.com/blog/wp-json/wp/v2/posts"
payload = {}
headers = {}
response = requests.request("GET", url, headers=headers, data=payload)
print(response.text)</code>
      </div>
      <div class="secondary">
         <h3>Arguments</h3>
         <table class="arguments">
            <tr>
               <td>
                  <code>context</code><br />
               </td>
               <td>
                  <p>Scope under which the request is made; determines fields present in response.</p>
                  <p class="default">
                     Default: <code>view</code>
                  </p>
                  <p>One of: <code>view</code>, <code>embed</code>, <code>edit</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>page</code><br />
               </td>
               <td>
                  <p>Current page of the collection.</p>
                  <p class="default">
                     Default: <code>1</code>
                  </p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>per_page</code><br />
               </td>
               <td>
                  <p>Maximum number of items to be returned in result set.</p>
                  <p class="default">
                     Default: <code>10</code>
                  </p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>search</code><br />
               </td>
               <td>
                  <p>Limit results to those matching a string.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>after</code><br />
               </td>
               <td>
                  <p>Limit response to posts published after a given ISO8601 compliant date.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>modified_after</code><br />
               </td>
               <td>
                  <p>Limit response to posts modified after a given ISO8601 compliant date.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>author</code><br />
               </td>
               <td>
                  <p>Limit result set to posts assigned to specific authors.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>author_exclude</code><br />
               </td>
               <td>
                  <p>Ensure result set excludes posts assigned to specific authors.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>before</code><br />
               </td>
               <td>
                  <p>Limit response to posts published before a given ISO8601 compliant date.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>modified_before</code><br />
               </td>
               <td>
                  <p>Limit response to posts modified before a given ISO8601 compliant date.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>exclude</code><br />
               </td>
               <td>
                  <p>Ensure result set excludes specific IDs.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>include</code><br />
               </td>
               <td>
                  <p>Limit result set to specific IDs.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>offset</code><br />
               </td>
               <td>
                  <p>Offset the result set by a specific number of items.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>order</code><br />
               </td>
               <td>
                  <p>Order sort attribute ascending or descending.</p>
                  <p class="default">
                     Default: <code>desc</code>
                  </p>
                  <p>One of: <code>asc</code>, <code>desc</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>orderby</code><br />
               </td>
               <td>
                  <p>Sort collection by post attribute.</p>
                  <p class="default">
                     Default: <code>date</code>
                  </p>
                  <p>One of: <code>author</code>, <code>date</code>, <code>id</code>, <code>include</code>, <code>modified</code>, <code>parent</code>, <code>relevance</code>, <code>slug</code>, <code>include_slugs</code>, <code>title</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>search_columns</code><br />
               </td>
               <td>
                  <p>Array of column names to be searched.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>slug</code><br />
               </td>
               <td>
                  <p>Limit result set to posts with one or more specific slugs.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>status</code><br />
               </td>
               <td>
                  <p>Limit result set to posts assigned one or more statuses.</p>
                  <p class="default">
                     Default: <code>publish</code>
                  </p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>tax_relation</code><br />
               </td>
               <td>
                  <p>Limit result set based on relationship between multiple taxonomies.</p>
                  <p>One of: <code>AND</code>, <code>OR</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>categories</code><br />
               </td>
               <td>
                  <p>Limit result set to items with specific terms assigned in the categories taxonomy.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>categories_exclude</code><br />
               </td>
               <td>
                  <p>Limit result set to items except those with specific terms assigned in the categories taxonomy.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>tags</code><br />
               </td>
               <td>
                  <p>Limit result set to items with specific terms assigned in the tags taxonomy.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>tags_exclude</code><br />
               </td>
               <td>
                  <p>Limit result set to items except those with specific terms assigned in the tags taxonomy.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>sticky</code><br />
               </td>
               <td>
                  <p>Limit result set to items that are sticky.</p>
               </td>
            </tr>
         </table>
      </div>
   </section>
   <section class="route">
      <div class="primary">
         <h2>Create a Post</h2>
       <h3>Definition</h3>
         <code>POST https://beztbetz.com/blog/wp-json/wp/v2/posts</code> <br/><br/>
        <b>Authorization ( Basic Auth ) </b><br/>
         Username : <br/>
         Password : <br/>
         <h2>Required Arguments : title, content, featured_media, categories, tags (optional)</h2>
         <p>In order Create Post, first <b>Create Media</b> it'll rerutn <b>ID</b> add it to <b>featured_media</b> </p>
         <h3>Example Request</h3>
         <code>import requests
import json
url = "https://beztbetz.com/blog/wp-json/wp/v2/posts"
payload = json.dumps({
  "title": "Manoj Test Post",
  "status": "publish",
  "content": "Test Manoj Post Content....",
  "featured_media": 265
})
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Basic YmV6dGJldHo6VThQZSBUWWQ0IHpsOVkgWk42ViBrdU9GIE9XQXI='
}
response = requests.request("POST", url, headers=headers, data=payload)
print(response.text)
</code>
         <h3>Arguments</h3>
         <table class="arguments">
            <tr>
               <td>
                  <code><a href="#schema-date">date</a></code><br />
               </td>
               <td>
                  <p>The date the post was published, in the site&#039;s timezone.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-date_gmt">date_gmt</a></code><br />
               </td>
               <td>
                  <p>The date the post was published, as GMT.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-slug">slug</a></code><br />
               </td>
               <td>
                  <p>An alphanumeric identifier for the post unique to its type.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-status">status</a></code><br />
               </td>
               <td>
                  <p>A named status for the post.</p>
                  <p>One of: <code>publish</code>, <code>future</code>, <code>draft</code>, <code>pending</code>, <code>private</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-password">password</a></code><br />
               </td>
               <td>
                  <p>A password to protect access to the content and excerpt.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-title">title</a></code><br />
               </td>
               <td>
                  <p>The title for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-content">content</a></code><br />
               </td>
               <td>
                  <p>The content for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-author">author</a></code><br />
               </td>
               <td>
                  <p>The ID for the author of the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-excerpt">excerpt</a></code><br />
               </td>
               <td>
                  <p>The excerpt for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-featured_media">featured_media</a></code><br />
               </td>
               <td>
                  <p>The ID of the featured media for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-comment_status">comment_status</a></code><br />
               </td>
               <td>
                  <p>Whether or not comments are open on the post.</p>
                  <p>One of: <code>open</code>, <code>closed</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-ping_status">ping_status</a></code><br />
               </td>
               <td>
                  <p>Whether or not the post can be pinged.</p>
                  <p>One of: <code>open</code>, <code>closed</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-format">format</a></code><br />
               </td>
               <td>
                  <p>The format for the post.</p>
                  <p>One of: <code>standard</code>, <code>aside</code>, <code>chat</code>, <code>gallery</code>, <code>link</code>, <code>image</code>, <code>quote</code>, <code>status</code>, <code>video</code>, <code>audio</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-meta">meta</a></code><br />
               </td>
               <td>
                  <p>Meta fields.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-sticky">sticky</a></code><br />
               </td>
               <td>
                  <p>Whether or not the post should be treated as sticky.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-template">template</a></code><br />
               </td>
               <td>
                  <p>The theme file to use to display the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-categories">categories</a></code><br />
               </td>
               <td>
                  <p>The terms assigned to the post in the category taxonomy.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-tags">tags</a></code><br />
               </td>
               <td>
                  <p>The terms assigned to the post in the post_tag taxonomy.</p>
               </td>
            </tr>
         </table>
      </div>
<!--       <div class="secondary">
         <h3>Definition</h3>
         <code>POST https://beztbetz.com/blog/wp-json/wp/v2/posts </code>
      </div> -->
   </section>
   <section class="route">
      <div class="primary">
         <h2>Retrieve a Post</h2>
         <h3>Definition</h3>
         <code>GET https://beztbetz.com/blog/wp-json/wp/v2/posts/{{postId}} </code>
         <p>Query this endpoint to retrieve a specific post record.</p> <br/><br/>
         <b>Authorization ( Basic Auth ) </b><br/>
         Username : <br/>
         Password : <br/>
         <h2>Required Arguments : title, content, featured_media, categories, tags (optional)</h2>
         <h3>Example Request</h3>
         <code>import requests
url = "https://beztbetz.com/blog/wp-json/wp/v2/posts/{{postId}}"
payload = {}
headers = {
  'Authorization': 'Basic d2FwaTptWmJ1IFRoUEkgYmJwdiBSUjRMIEFzZnYgdjNBeQ=='
}
response = requests.request("GET", url, headers=headers, data=payload)
print(response.text)
</code>
      </div>
      <div class="secondary">
         <h3>Arguments</h3>
         <table class="arguments">
            <tr>
               <td>
                  <code>id</code><br />
               </td>
               <td>
                  <p>Unique identifier for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>context</code><br />
               </td>
               <td>
                  <p>Scope under which the request is made; determines fields present in response.</p>
                  <p class="default">
                     Default: <code>view</code>
                  </p>
                  <p>One of: <code>view</code>, <code>embed</code>, <code>edit</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>password</code><br />
               </td>
               <td>
                  <p>The password for the post if it is password protected.</p>
               </td>
            </tr>
         </table>
      </div>
   </section>
   <section class="route">
    <h2>Update a Post</h2>
    <div class="primary">
         <h3>Definition</h3>
         <code>POST https://beztbetz.com/blog/wp-json/wp/v2/posts/267?categories=5,3&tags=7,8,10</code>
         <h2>Required Arguments : title, content, featured_media, categories, tags (optional)</h2>
         <h3>Example Request</h3> 
         <code>import requests
url = "https://beztbetz.com/blog/wp-json/wp/v2/posts/267?categories=5,3&tags=7,8,10"
payload = {}
files={}
headers = {
  'Authorization': 'Basic YmV6dGJldHo6VThQZSBUWWQ0IHpsOVkgWk42ViBrdU9GIE9XQXI='
}
response = requests.request("POST", url, headers=headers, data=payload, files=files)
print(response.text)
</code>
      </div>
      <div class="secondary">
         <h3>Arguments</h3>
         <table class="arguments">
            <tr>
               <td>
                  <code><a href="#schema-id">id</a></code><br />
               </td>
               <td>
                  <p>Unique identifier for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-date">date</a></code><br />
               </td>
               <td>
                  <p>The date the post was published, in the site&#039;s timezone.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-date_gmt">date_gmt</a></code><br />
               </td>
               <td>
                  <p>The date the post was published, as GMT.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-slug">slug</a></code><br />
               </td>
               <td>
                  <p>An alphanumeric identifier for the post unique to its type.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-status">status</a></code><br />
               </td>
               <td>
                  <p>A named status for the post.</p>
                  <p>One of: <code>publish</code>, <code>future</code>, <code>draft</code>, <code>pending</code>, <code>private</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-password">password</a></code><br />
               </td>
               <td>
                  <p>A password to protect access to the content and excerpt.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-title">title</a></code><br />
               </td>
               <td>
                  <p>The title for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-content">content</a></code><br />
               </td>
               <td>
                  <p>The content for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-author">author</a></code><br />
               </td>
               <td>
                  <p>The ID for the author of the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-excerpt">excerpt</a></code><br />
               </td>
               <td>
                  <p>The excerpt for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-featured_media">featured_media</a></code><br />
               </td>
               <td>
                  <p>The ID of the featured media for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-comment_status">comment_status</a></code><br />
               </td>
               <td>
                  <p>Whether or not comments are open on the post.</p>
                  <p>One of: <code>open</code>, <code>closed</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-ping_status">ping_status</a></code><br />
               </td>
               <td>
                  <p>Whether or not the post can be pinged.</p>
                  <p>One of: <code>open</code>, <code>closed</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-format">format</a></code><br />
               </td>
               <td>
                  <p>The format for the post.</p>
                  <p>One of: <code>standard</code>, <code>aside</code>, <code>chat</code>, <code>gallery</code>, <code>link</code>, <code>image</code>, <code>quote</code>, <code>status</code>, <code>video</code>, <code>audio</code></p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-meta">meta</a></code><br />
               </td>
               <td>
                  <p>Meta fields.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-sticky">sticky</a></code><br />
               </td>
               <td>
                  <p>Whether or not the post should be treated as sticky.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-template">template</a></code><br />
               </td>
               <td>
                  <p>The theme file to use to display the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-categories">categories</a></code><br />
               </td>
               <td>
                  <p>The terms assigned to the post in the category taxonomy.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code><a href="#schema-tags">tags</a></code><br />
               </td>
               <td>
                  <p>The terms assigned to the post in the post_tag taxonomy.</p>
               </td>
            </tr>
         </table>
      </div>
      
   </section>
   <section class="route">
    <h2>Delete a Post</h2>
    <div class="secondary">
         <h3>Definition</h3>
         <code>DELETE https://beztbetz.com/blog/wp-json/wp/v2/posts/{{postId}}</code>
         <h2>Required Arguments : id (Post ID)</h2>
         <h3>Example Request</h3>
         <code>import requests
url = "https://beztbetz.com/blog/wp-json/wp/v2/posts/{{postId}}"
payload = {}
headers = {
  'Authorization': 'Basic d2FwaTptWmJ1IFRoUEkgYmJwdiBSUjRMIEFzZnYgdjNBeQ=='
}
response = requests.request("DELETE", url, headers=headers, data=payload)
print(response.text)
</code>
      </div>
      <div class="primary">
         <h3>Arguments</h3>
         <table class="arguments">
            <tr>
               <td>
                  <code>id</code><br />
               </td>
               <td>
                  <p>Unique identifier for the post.</p>
               </td>
            </tr>
            <tr>
               <td>
                  <code>force</code><br />
               </td>
               <td>
                  <p>Whether to bypass Trash and force deletion.</p>
               </td>
            </tr>
         </table>
      </div>
      
   </section>

 <section class="route">
   <div class="primary">
      <h2>Schema</h2>
      <p>The schema defines all the fields that exist within a post record. Any response from these endpoints can be expected to contain the fields below unless the `_filter` query parameter is used or the schema field only appears in a specific context.</p>
      <table class="attributes">
         <tr id="schema-id">
            <td>
               <code>id</code>
            </td>
            <td>
               <p>Unique identifier for the post.</p>
               <p class="type">
                  JSON data type: integer				
               </p>
               <p class="read-only">Read only</p>
               <p class="context">Context: <code>view</code>, <code>edit</code>, <code>embed</code></p>
            </td>
         </tr>
         <tr id="schema-slug">
            <td>
               <code>slug</code>
            </td>
            <td>
               <p>An alphanumeric identifier for the post unique to its type.</p>
               <p class="type">
                  JSON data type: string				
               </p>
               <p class="context">Context: <code>view</code>, <code>edit</code>, <code>embed</code></p>
            </td>
         </tr>
         <tr id="schema-status">
            <td>
               <code>status</code>
            </td>
            <td>
               <p>A named status for the post.</p>
               <p class="type">
                  JSON data type: string				
               </p>
               <p class="context">Context: <code>view</code>, <code>edit</code></p>
               <p>One of: <code>publish</code>, <code>future</code>, <code>draft</code>, <code>pending</code>, <code>private</code></p>
            </td>
         </tr>
         <tr id="schema-generated_slug">
            <td>
               <code>generated_slug</code>
            </td>
            <td>
               <p>Slug automatically generated from the post title.</p>
               <p class="type">
                  JSON data type: string				
               </p>
               <p class="read-only">Read only</p>
               <p class="context">Context: <code>edit</code></p>
            </td>
         </tr>
         <tr id="schema-title">
            <td>
               <code>title</code>
            </td>
            <td>
               <p>The title for the post.</p>
               <p class="type">
                  JSON data type: object				
               </p>
               <p class="context">Context: <code>view</code>, <code>edit</code>, <code>embed</code></p>
            </td>
         </tr>
         <tr id="schema-content">
            <td>
               <code>content</code>
            </td>
            <td>
               <p>The content for the post.</p>
               <p class="type">
                  JSON data type: object				
               </p>
               <p class="context">Context: <code>view</code>, <code>edit</code></p>
            </td>
         </tr>
         <tr id="schema-featured_media">
            <td>
               <code>featured_media</code>
            </td>
            <td>
               <p>The ID of the featured media for the post.</p>
               <p class="type">
                  JSON data type: integer				
               </p>
               <p class="context">Context: <code>view</code>, <code>edit</code>, <code>embed</code></p>
            </td>
         </tr>
         <tr id="schema-categories">
            <td>
               <code>categories</code>
            </td>
            <td>
               <p>The terms assigned to the post in the category taxonomy.</p>
               <p class="type">
                  JSON data type: array				
               </p>
               <p class="context">Context: <code>view</code>, <code>edit</code></p>
            </td>
         </tr>
         <tr id="schema-tags">
            <td>
               <code>tags</code>
            </td>
            <td>
               <p>The terms assigned to the post in the post_tag taxonomy.</p>
               <p class="type">
                  JSON data type: array				
               </p>
               <p class="context">Context: <code>view</code>, <code>edit</code></p>
            </td>
         </tr>
      </table>
   </div>
</section>

</div>
