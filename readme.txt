DayZ Chernarus Novodmitrovsk Bunker Custom Structure Json File For Console and PC Instructions & Terms Of Use

ONLY WORKS ON DAYZ 1.19 AND LATER!!!! NOT EARLIER VERSIONS!!!

Spawns a bunker with gear in Novodmitrovsk at 11344.60 / 14701.86, access from the roof of the building requiring a punched key access card, on Chernarus.

Limited Testing on PC Chernarus Local Server DAYZ Version 1.19 October 2022.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

If you'd like to edit & customize my bunker, simply load "novotestbunker.dze" into DayZ Editor.

Many Thanks To Inclement Dab for his amazing DayZ Editor that makes this all possible: https://steamcommunity.com/sharedfiles/filedetails/?id=2250764298

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Stop your server.

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "novybunker.json" from the extracted files to inside the "custom" folder of the mission directory on your server.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "objectSpawnersArr" line.

This file tells your server to access your custom file.

Edit it to look like this: 

	"objectSpawnersArr": ["custom/novybunker.json"],	
	
If you already are calling custom jsons to spawn items or buildings, seperate the files like this:

	"objectSpawnersArr": ["custom/novybunker.json","custom/anotherfile.json","custom/differentfile.json"],
	
Save your changes & upload if you need to.

TO SPAWN THE KEY CARD ON CHERNARUS IN THE PERMANENT TOXIC ZONES, ADD THIS LINE TO YOUR types.xml :

 <type name="PunchedCard">
        <nominal>2</nominal>
        <lifetime>14400</lifetime>
        <restock>0</restock>
        <min>2</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0"/>
        <category name="weapons"/>
        <usage name="ContaminatedArea"/>
    </type>
	
Save your changes & upload if you need to.

Restart your server and the new objects will appear immediatly.

Thanks, Rob.
