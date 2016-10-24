## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
rails new  

2. What do Models generally inherit from in rails?  
ActiveRecord::Base

3. What do Controllers generally inherit from in a rails project?
ApplicationController  

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?  
resources :horses, only [:show]  

5. What rake task is useful when looking at routes, and what information does it give you?  
rake routes  

6. What is an example of a route helper? When would you use them?  
company_path(company)  You use this when building a link as well as in a feature test.  

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?  
_path gives you the relative path while _url gives you the whole url  

8. What are strong params and why are the necessary?  
This checks to make sure that objects are getting created with the correctly correlated info.  

9. What role does `form_for` play in helping us create our forms?  
It builds the html form as well as passes the information on to create/update tied to the right keys.  

10. How does `form_for` know where to submit the user's input?  
..It uses the input instance variable in combination with the type of page it came from (new/edit)

11. Create a form using a `form_for` helper to create a new `Horse`.   
form_for @horse do |f|  
f.label :name  
f.text_field :name  

f.label :age
f.text_field :age  

f.submit
end   

12. Why do we want to validate our models?  
We validate our models to ensure that our database is normative and to ensure the correct kind of information is being passed through. 
