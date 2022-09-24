# Android_Alert_Dialog
Creating An Alert Dialog for Exiting the app (Exit Confirmation)

This topic is a part of [My Complete Andorid Course](https://github.com/ananddasani/Android_Apps)

# Code

#### 1st Activity 
```
      button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                new AlertDialog.Builder(MainActivity.this)
                        .setIcon(R.drawable.warning)
                        .setTitle("Exit !!")
                        .setMessage("Do you really want to Exit?")
                        .setPositiveButton("Yes", new DialogInterface.OnClickListener() {
                            @Override
                            public void onClick(DialogInterface dialog, int which) {
                                finish();
                            }
                        })
                        .setNegativeButton("No", new DialogInterface.OnClickListener() {
                            @Override
                            public void onClick(DialogInterface dialog, int which) {
                                dialog.dismiss();
                            }
                        })
                        .setNeutralButton("Help", new DialogInterface.OnClickListener() {
                            @Override
                            public void onClick(DialogInterface dialog, int which) {
                                Toast.makeText(MainActivity.this, "Press Yes to Exit", Toast.LENGTH_SHORT).show();
                            }
                        })
                        .show();
            }
        });
        
        
        
     //back button is pressed
    @Override
    public void onBackPressed() {
        new AlertDialog.Builder(MainActivity.this)
                .setIcon(R.drawable.warning)
                .setTitle("Exit !!")
                .setMessage("Do you really want to Exit?")
                .setPositiveButton("Yes", new DialogInterface.OnClickListener() {
                    @Override
                    public void onClick(DialogInterface dialog, int which) {
                        finish();
                    }
                })
                .setNegativeButton("No", new DialogInterface.OnClickListener() {
                    @Override
                    public void onClick(DialogInterface dialog, int which) {
                        dialog.dismiss();
                    }
                })
                .setNeutralButton("Help", new DialogInterface.OnClickListener() {
                    @Override
                    public void onClick(DialogInterface dialog, int which) {
                        Toast.makeText(MainActivity.this, "Press Yes to Exit", Toast.LENGTH_SHORT).show();
                    }
                })
                .show();
    }
```

# App Highlight

![Alert Dialog Default App](https://user-images.githubusercontent.com/74413402/192093129-22e493af-24fd-489b-bf5b-c97a98e4c101.png)
![Alert Dialog Default Code](https://user-images.githubusercontent.com/74413402/192093136-974a1a21-64fc-41e9-86b0-b0436c832033.png)

