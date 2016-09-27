## laios10appdevesst2
###1 Basic IOS UI



###2 Auto Layout
####1. Auto Layout fundamentals
right click label, drag to storyboard edge, choose leading space to container margin/vertical spacing to top layout guide  

For labels at right side: trailinging space to containing margin/vertical spacing to top layout guide.  

We will deal with orange line next lec.

####2 Auto Layout issues
click the yellow ball ->exclaimation mark->update frames->fix misplacement



####3 Modify constraints with the Size Inspector

####4 Automatically expand object sizes with constraints
4 buttons: stack,align,pin,resolve auto layout issues.  

Another way to pin:  
pin->add constraints  

####6 Pin an object to its nearest neighbor
Select trailing space to superview. The superview is the view in which another view is contained.  


content hugging priority( which objects expand or contract. Which ones get preference.)  

Lower number gives it priority.  


###3 More UI Objects
####1 The Date Picker control
Date picker->select->b4->reset to suggested constraints (o s cmd =)

####2 Handle the value changed event
system editor->option+click the swift class want to edit.  

set both IBOutlet and IBAction for datepicker.

####3
```
@IBOutlet weak var picker: UIDatePicker!
@IBOutlet weak var label: UILabel!
override func viewDidLoad(){
  pickerDidChange(picker)
}


@IBAction func pickerDidChange(_ sender:AnyObject){
  let date:Date=picker.date
  let formatter:DateFormatter = DateFormatter()
  formatter.dateForamat="EEEE"
  let datOfWeek:String = formatter.string(from:date)
  label.text = "\(dayOfWeek)"
}
```
