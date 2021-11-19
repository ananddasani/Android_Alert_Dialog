# Android_Alert_Dialog
Creating An Alert Dialog for Exiting the app (Exit Confirmation)

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

<img src="app_images/Alert Dialog Default Code.png" width="1000" /><br>

<img src="app_images/Alert Dialog Default App.png" width="300" /><br>
