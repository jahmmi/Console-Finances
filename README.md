# Console Finances

This is a work with arrays makinf a finances


## Authors

- [@jahmmi](https://github.com/jahmmi)


## Deployment

https://jahmmi.github.io/Console-Finances/ 
and press F12 or right click -> inspect -> Console


## Usage/Examples

```javascript
// Get the total number of months in the dataset
    var months = finances.length;
    
    // Get the total amount of money in the dataset
    var total = 0;
    for (var i = 0; i < finances.length; i++) {
        total += finances[i][1];
    }
    
    // Get the average change in "Profit/Losses" between months over the entire period
    var averageChange = 0;
    for (var i = 1; i < finances.length; i++) {
        averageChange += finances[i][1] - finances[i - 1][1];
    }
    averageChange /= finances.length - 1;
    
    // Get the greatest increase in profits (date and amount) over the entire period
    var maxChange = 0;
    var maxChangeDate = '';
    for (var i = 1; i < finances.length; i++) {
        var change = finances[i][1] - finances[i - 1][1];
        if (change > maxChange) {
            maxChange = change;
            maxChangeDate = finances[i][0];
        }
    }
    
    // Get the greatest decrease in losses (date and amount) over the entire period
    var minChange = 0;
    var minChangeDate = '';
    for (var i = 1; i < finances.length; i++) {
        var change = finances[i][1] - finances[i - 1][1];
        if (change < minChange) {
            minChange = change;
            minChangeDate = finances[i][0];
        }
    }
    
    // Print the results
    console.log("Financial Analysis");
    console.log("----------------------------");
    console.log("Total Months: " + months);
    console.log("Total: " + total);
    console.log("Average  Change: " + Math.ceil(averageChange));
    console.log("Greatest Increase in Profits: " + maxChangeDate + " ($" + maxChange + ")");
    console.log("Greatest Decrease in Profits: " + minChangeDate + " ($" + minChange + ")");
    


## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Feedback

If you have any feedback, please reach out to me at lozeviliq3@gmail.com

