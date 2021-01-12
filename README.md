# Theatre_Vertigo_C#_Project
Hi, my name is Dave Street. I completed Software Developer Boot Camp and earned my certification from The Tech Academy. This was an intership experience  with Prosper I.T. Consulting. This project was a great experience for me using Agile/Scrum methodologies during this two week sprint.
<br>![theatreAbout](https://user-images.githubusercontent.com/68976585/104261726-08a88e80-543b-11eb-90a5-e1bff0b7a901.png)<br>
Working with C# on Theatre Vertigo website completing these tasks:
- Create a New User easy login for development purposes.

- Create a new Donation Model table in the database with a one to many relationship between the AppUser (or Donor) and Donation including a timestamp at time of donation. Here is a code sample:
```
namespace TheatreCMS.Models
{
    public class Donation
    {
        public Donation()  // donation constructor
        {
            DonationTime = DateTime.Now;    //with dateTime at instatiation of object
        }

        [Key]                                    // primary key
        public int DonationId { get; set; }
        public DateTime DonationTime { get; set; }
        public int Amount { get; set; }

        public ApplicationUser Donor { get; set; }  // set foreign key to ApplicationuUser id with Donor
    }
}
```
- Create an Admin field for a visiting theatre company’s name to be displayed in the About section and be easily updated as desired. This included helping to phase out an older reader method and update using Json properties instead.
![adminField](https://user-images.githubusercontent.com/68976585/104261717-06463480-543b-11eb-95d9-4c186aeb927f.png)
![theatreAbout](https://user-images.githubusercontent.com/68976585/104261726-08a88e80-543b-11eb-90a5-e1bff0b7a901.png)
- Create a new Rental History Model table in the database with a fully defined one to many relationship between the AppUser (or Renter) and Rental History. Here is a code sample of that:
```
namespace TheatreCMS.Models
{
    public class RentalHistory
    {
        [Key]
        public int RentalHistoryId { get; set; }

        public ApplicationUser Renter { get; set; }
        public Rental Rental { get; set; }
        public int RentalId { get; set; }
        public bool RentalDamaged { get; set; }
        public string DamagesIncurred { get; set; }

    }
}

```
