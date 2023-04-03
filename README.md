# Movie-ticket-booking-system
Skip to content
Search or jump to…
Pull requests
Issues
Codespaces
Marketplace
Explore
 
@Rajathshanbhag97 
meet-gfg
/
movieshark
Public
Fork your own copy of meet-gfg/movieshark
Code
Issues
Pull requests
Actions
Projects
Security
Insights
movieshark/design.txt

meet-gfg Project commit
Latest commit 6194d65 on Oct 9, 2022
 History
 0 contributors
102 lines (83 sloc)  1.82 KB
 

Project 2

MovieShark --> Movie ticket booking system


Requirements:
    a.	Search a movie by title
    b.	Rate and add review for a movie
    c.	Search a top 5 movie by genre
    d.  Search shows running in a city
    e.  book ticket for the show
    d.  send notification to user for the booked tickets.


Entity:
    Movie:{
        --Must to have
        Id,
        title,
        genre,
        rating,
        <reviews>
        <shows>
       -- Good to have
        Release date
        Length
       -- Nice to have
        Cast
        }
    Review: {
       -- Must to have
        Id,
        movieTitle,
        rating,
        review
      --  Good to have
        Userid,
        createdAt,
        }

        Theater:{
        Id,
        name,
        seats,
        city,
        address,
        }

        TheaterSeat:{
        Id,
        number,
        type
        }

        Show:{
        id,
        movie,
        theater,
        time,
        tickets,
        seats

        }
        showSeat{
        Id,
        type,
        price,
        show,
        --IMP isBooked
        }


Entity relation:
One movie can contain many reviews  -> One to many relationship.
One Theater contains many seats  -> One to many relationship.
One Movie contains many shows -> One to many
One Show contains many seats -> One to many
One User contains many bookings -> One to many



APIs:
        addMovie ->POST
        updateMovie -> PUT
        deleteMovie -> DELETE
        addTheater -> POST
        addTheaterSeat -> POST // optional for later
        addUser -> POST
        addShow -> POST
        SearchByTitle -> GET
        AddReview -> POST
        SearchByGenre -> GET
        SearchByCity -> GET
        SearchByShow -> GET
        searchUser ->GET





APIs:
#Postman collection added in the root folder, import to use all apis.
Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
movieshark/design.txt at master · meet-gfg/movieshark
