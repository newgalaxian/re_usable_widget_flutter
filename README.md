# Reusable widgets in Flutter


Card with radius
-----------------

    Card(
      shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.circular(16.0),
      ),
      elevation: 5,
      margin: EdgeInsets.all(10),
      color: color,
      child: Padding(
        padding: const EdgeInsets.all(16.0),
        child: Text(
          text,
          textAlign: TextAlign.center,
          style: TextStyle(
            fontSize: 20.0,
            color: Colors.white,
          ),
        ),
      ),
    ),

 Clickable Card 
 -------------
 InkWell() gives clickable property
 
     InkWell(
    onTap: () {
      scaffoldKey.currentState.showSnackBar(snackBar);
    },
    child: Card(....
    ....
    ....)
    
 Making widget Reusable
 --------------
 
     Widget _card(Color color, String text) { //color and text added ,you can add more ..
     return InkWell(
     onTap: () {
      scaffoldKey.currentState.showSnackBar(snackBar);
     },
     child: Card(
      shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.circular(16.0),
      ),
      elevation: 5,
      margin: EdgeInsets.all(10),
      color: color,
      child: Padding(
        padding: const EdgeInsets.all(16.0),
        child: Text(
          text,
          textAlign: TextAlign.center,
          style: TextStyle(
            fontSize: 20.0,
            color: Colors.white,
          ),
        ),
      ),
     ),
    );
    }
    
 ----------------------------------
 
 Using this widget
 -----------
 Using ListView for inbuild scrolling
 
     ListView(
        children: [
          Column(
            mainAxisAlignment: MainAxisAlignment.start,
            crossAxisAlignment: CrossAxisAlignment.stretch,
            children: [
            
              _card(Colors.blue, 'from widget'), // using card widget and changing colors and text
              _card(Colors.green, 'green'),
              ],
              ),
              );
              
  -------------------------    
  
  
<img src="https://github.com/newgalaxian/re_usable_widget/blob/master/re_usable_widget_1.jpg" alt="eusable widgets" >

<img src="https://github.com/newgalaxian/re_usable_widget/blob/master/re_usable_widget_2.jpg" alt="eusable widgets" >



## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
