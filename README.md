# CSharpLiveProject

For the last two weeks at The Tech Academy, I worked with my peers in a team developing a full scale MVC Web Application in C#. This was a great learning experience that included fixing bugs cleaning up code, and adding requested features. I worked on a few front end stories and I attempted to completed a very large back end story the last week of the sprint. I am very proud of my progress during this sprint, not only because I completed the challenging front end stories, but the back end story I attempted was a great learning experience as well. The two week sprint also exposed us to the agile process and daily stand-ups helped improve productivity greatly. It was a chance for us to come together as a group to discuss what we were working on. I am confident I will use these skills again in the future. 

Below are descriptions of the stories I worked on along with code snippets.

# Front End Stories

# 1) Unregistered Users card-style Tweak
On the Users / Index View page, the Admin is able to view All Users List (Active, Suspended and unregistered) gathered in one. But there seems to be some card style inconsistency with the Unregistered Users list. Make sure the card style looks similar and consistent with the other two (Active, Suspended). 

<div class="card mt-5">
        <div class="card-header card-header-bg">
            <div class="row">
                <div class="col-sm">
                    <h3>User List</h3>
                </div>
                <div class="col-sm">
                    <h4>@Html.ActionLink("Create User", "Create", "CreateUserRequest", null, new { @class = "float-right text-dark" })</h4>
                </div>
            </div>
        </div>
        <div class="card-body">
            @{Html.RenderAction("_UserList", "Users");}
        </div>
        <div class="card-body">
            @{Html.RenderAction("_SuspendedUsers", "Users");}
        </div>
        <div class="card-body">
            @{ Html.RenderAction("_UnregisteredUsers", "Users");}
        </div>
    </div>
    
# 2) Color palette implementation
Now that we have our Container Agreement story complete and integrated into the master branch, it's time to use the Color-palette prepared for the entire site. (see the image  "Colorpalette2.png" in Content/images folder) . All the color style used in the entire site should make use of NO other color but these given colors only. These colors are names as root colors at the top of the Site.css page to make them easier to apply.

The style for all view pages should also be consistent and similar to each other.  (Tips:  All Index and Create pages can have the same background-color while all edit/detail/delete view pages can use another bg-color).

In some cases, you will encounter that your style changes may not be applied to some containers. This could be because the id attribute taking precedence over class declarations. Find a way to fix these issues too. 

-Added required color palette colors to various css styles to stay consistent with design pattern and corrected overriding classes/id's.
