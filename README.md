# Weather4cast---Practicum
This is my Practicum Project for Introduction to Mobile Development Module.
1st Page code( Splash Page/Screen) - I used Canva to Design my own logo.
import android.content.Intent
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.Image
import androidx.compose.foundation.layout.Arrangement
import androidx.compose.foundation.layout.Column
import androidx.compose.foundation.layout.Spacer
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.foundation.layout.fillMaxWidth
import androidx.compose.foundation.layout.height
import androidx.compose.foundation.layout.size
import androidx.compose.foundation.shape.CircleShape
import androidx.compose.material3.Button
import androidx.compose.material3.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.draw.clip
import androidx.compose.ui.platform.LocalContext
import androidx.compose.ui.res.painterResource
import androidx.compose.ui.tooling.preview.Preview
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp
import com.example.weather4cast.ui.theme.Weather4castTheme

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            Weather4castTheme {
                    Weather4cast()
                }
            }
        }
    }


@Composable
fun Weather4cast(modifier: Modifier = Modifier) {
    val sImage = painterResource(R.drawable.weather4cast)
    val context = LocalContext.current

    Column(
        modifier = Modifier.fillMaxSize(),
        horizontalAlignment = Alignment.CenterHorizontally
    ) {
        Text(
            text = "Weather4cast",
            fontSize = 25.sp
        )
        Image(
            painter = sImage,
            contentDescription = "Splash Screen",
            modifier = Modifier
                .size(200.dp)
                .clip(shape = CircleShape)
        )
        Button(onClick = {
            var navigate = Intent(context, MainActivity2::class.java)
            context.startActivity(navigate)
        }) {
            Text(text = "START")
        }
        Spacer(modifier = Modifier.height(350.dp))

        Column(
            modifier = Modifier.fillMaxWidth(),
            verticalArrangement = Arrangement.Bottom
        ) {
                Text(text = "Lucky Tshishonga Maiwashe of Student ID: ST10245512")
        }

    }
}

    @Preview(showBackground = true)
    @Composable
    fun GreetingPreview() {
        Weather4castTheme {
            Weather4cast()
        }
    }

2nd Page(The Main Page/Screen) - I drew a mock up of how i wanted the UI to look and i started building it with my code in Android Studio.
import android.content.Intent
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.Image
import androidx.compose.foundation.background
import androidx.compose.foundation.layout.Arrangement
import androidx.compose.foundation.layout.Column
import androidx.compose.foundation.layout.Row
import androidx.compose.foundation.layout.Spacer
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.foundation.layout.height
import androidx.compose.foundation.layout.padding
import androidx.compose.foundation.layout.size
import androidx.compose.foundation.layout.width
import androidx.compose.foundation.shape.CircleShape
import androidx.compose.material3.Button
import androidx.compose.material3.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Alignment
import androidx.compose.ui.Alignment.Companion.CenterHorizontally
import androidx.compose.ui.Modifier
import androidx.compose.ui.draw.clip
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.platform.LocalContext
import androidx.compose.ui.res.painterResource
import androidx.compose.ui.tooling.preview.Preview
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp
import com.example.weather4cast.ui.theme.Weather4castTheme

class MainActivity2 : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            Weather4castTheme {
                    Greeting()
                }
            }
        }
    }


@Composable
fun Greeting( modifier: Modifier = Modifier) {
    val today = painterResource(R.drawable.today)

    var context2 = LocalContext.current
    var contextback = context2
    var context4 = LocalContext.current


Column {
    Button(onClick = {
        var navigateBack = Intent(contextback, MainActivity::class.java)
        contextback.startActivity(navigateBack)
    }) {
        Text(text = "Back")
    }
}
    Column (
        modifier = Modifier.fillMaxSize(),
        horizontalAlignment = CenterHorizontally
    ){
        Text(
            text = "Weather4cast",
            fontSize = 15.sp
        )
        Spacer(modifier = Modifier.height(16.dp))
        Image(painter = today, contentDescription = "Today's Weather",
                modifier = Modifier
                    .size(230.dp)
                    .clip(shape = CircleShape))
    }
    Spacer(modifier = Modifier.padding(16.dp))
    Row (modifier= Modifier.fillMaxSize(),
        verticalAlignment = Alignment.CenterVertically){
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp),

        ) {
            Button(onClick = {
                var navigate2 =Intent(context2, MainActivity3::class.java)
                context2.startActivity(navigate2)
            }) {
                Text(text = "Mon")
            }

        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Button(onClick = {
                var navigate2 =Intent(context2, MainActivity3::class.java)
                context2.startActivity(navigate2)
            }) {
                Text(text = "Tue")
            }
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Button(onClick = {
                var navigate2 =Intent(context2, MainActivity3::class.java)
                context2.startActivity(navigate2) }) {
                Text(text = "Wed")
            }
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Button(onClick = {
                var navigate2 =Intent(context2, MainActivity3::class.java)
                context2.startActivity(navigate2)
            }) {
                Text(text = "Thur")
            }
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Button(onClick = {
                var navigate2 =Intent(context2, MainActivity3::class.java)
                context2.startActivity(navigate2)
            }) {
                Text(text = "Fri")
            }
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Button(onClick = {
                var navigate2 =Intent(context2, MainActivity3::class.java)
                context2.startActivity(navigate2) }) {
                Text(text = "Sat")
            }
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Button(onClick = {
                var navigate2 =Intent(context2, MainActivity3::class.java)
                context2.startActivity(navigate2) }) {
                Text(text = "Sun")
            }
        }
        }
    Row(modifier= Modifier.fillMaxSize(),
        verticalAlignment = Alignment.Bottom) {

        Button(onClick = {
            var navigate2 =Intent(context2, MainActivity3::class.java)
            context2.startActivity(navigate2)
        }) {
                Text(text = "Detailed View")

        }
        Button(onClick = {
            var navigate4 =Intent(context4, MainActivity4::class.java)
            context4.startActivity(navigate4)
        }) {
            Text(text = "Weekly Average")

        }

    }



}


@Preview(showBackground = true)
@Composable
fun GreetingPreview2() {
    Weather4castTheme {
        Greeting()
    }
}

3rd Page (The Detailed view page/Screen) This screen is supposed to give the user a more detailed view of the weather conditions on that day I'm still working on it.

import android.content.Intent
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.Image
import androidx.compose.foundation.background
import androidx.compose.foundation.layout.Arrangement
import androidx.compose.foundation.layout.Column
import androidx.compose.foundation.layout.Row
import androidx.compose.foundation.layout.Spacer
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.foundation.layout.height
import androidx.compose.foundation.layout.padding
import androidx.compose.foundation.layout.size
import androidx.compose.foundation.layout.width
import androidx.compose.foundation.shape.CircleShape
import androidx.compose.material3.Button
import androidx.compose.material3.MaterialTheme
import androidx.compose.material3.Surface
import androidx.compose.material3.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.draw.clip
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.platform.LocalContext
import androidx.compose.ui.res.painterResource
import androidx.compose.ui.tooling.preview.Preview
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp
import com.example.weather4cast.ui.theme.Weather4castTheme

class MainActivity3 : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            Weather4castTheme {
                // A surface container using the 'background' color from the theme
                Surface(
                    modifier = Modifier.fillMaxSize(),
                    color = MaterialTheme.colorScheme.background
                ) {
                    Greeting2()
                }
            }
        }
    }
}

@Composable
fun Greeting2(modifier: Modifier = Modifier) {
    val sunny = painterResource(R.drawable.sun)
    val cloudy = painterResource(R.drawable.cloudy__1_)
    val cold = painterResource(R.drawable.cold)
    val hot = painterResource(R.drawable.hot)
    val partlyCloudy = painterResource(R.drawable.partly_cloudy)
    val rain = painterResource(R.drawable.rain)
    var context3 = LocalContext.current
    var contextback2 = context3

    var days = arrayOf("Mon","Tuesday","Wednesday","Thursday","Friday","Saturday","Sunday")
    var temp = arrayOf(27,23,35,26,20,11,6)
    val contents = temp.contentToString()

    Spacer(modifier = Modifier.padding(16.dp))
    Row(
        modifier= Modifier.fillMaxSize(),
        verticalAlignment = Alignment.CenterVertically) {
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Text(text = "Mon")
            Image(painter = sunny, contentDescription = "Monday",
                modifier = Modifier
                    .size(70.dp)
                    .clip(shape = CircleShape)
            )
            Text(text = "27°C",
                fontSize = 28.sp)
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Text(text = "Tue")
            Image(painter = partlyCloudy, contentDescription = "Tuesday",
                modifier = Modifier
                    .size(70.dp)
                    .clip(shape = CircleShape)
            )
            Text(text = "23°C",
                fontSize = 28.sp)
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Text(text = "Wed")
            Image(painter = hot, contentDescription = "Wednesday",
                modifier = Modifier
                    .size(70.dp)
                    .clip(shape = CircleShape)
            )
            Text(text = "35°C",
                fontSize = 28.sp)
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Text(text = "Thur")
            Image(painter = sunny, contentDescription = "Thursday",
                modifier = Modifier
                    .size(70.dp)
                    .clip(shape = CircleShape)
            )
            Text(text = "26°C",
                fontSize = 28.sp)
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Text(text = "Fri")
            Image(
                painter = cloudy, contentDescription = "Friday",
                modifier = Modifier
                    .size(70.dp)
                    .clip(shape = CircleShape)
            )
            Text(text = "20°C",
                fontSize = 28.sp)
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Text(text = "Sat")
            Image(
                painter = rain, contentDescription = "Saturday",
                modifier = Modifier
                    .size(70.dp)
                    .clip(shape = CircleShape)
            )
            Text(text = "11°C",
                fontSize = 28.sp)
        }
        Spacer(modifier = Modifier.width(5.dp))
        Column(
            modifier = Modifier.background(Color.LightGray),
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {
            Text(text = "Sun")
            Image(painter = cold, contentDescription = "Sunday",
                modifier = Modifier
                    .size(70.dp)
                    .clip(shape = CircleShape)
            )
            Text(text = "6°C",
                fontSize = 28.sp)
        }

    }
    Row(
        modifier = Modifier.fillMaxSize(),
        verticalAlignment = Alignment.Top
        ) {
        Spacer(modifier = Modifier.height(25.dp))
        Button(onClick = {
            var navigateback2 = Intent(contextback2, MainActivity2::class.java)
            contextback2.startActivity(navigateback2)
        }) {
            Text(text = "Back")
        }
    }
}

@Preview(showBackground = true)
@Composable
fun GreetingPreview3() {
    Weather4castTheme {
        Greeting2()
    }
}
4th Page(Average weekly Temp)
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.material3.MaterialTheme
import androidx.compose.material3.Surface
import androidx.compose.material3.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.tooling.preview.Preview
import com.example.weather4cast.ui.theme.Weather4castTheme
import java.sql.Array

class MainActivity4 : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            Weather4castTheme {
                    Greeting3()
                }
            }
        }
    }


@Composable
fun Greeting3( modifier: Modifier = Modifier) {
    var days = arrayOf("Mon","Tuesday","Wednesday","Thursday","Friday","Saturday","Sunday")
    var temp = arrayOf(27,23,35,26,20,11,6)

    var i = intArrayOf(0+1+2+3+4+5+6)
    var ave = i



}

@Preview(showBackground = true)
@Composable
fun GreetingPreview4() {
    Weather4castTheme {
        Greeting3()
    }
