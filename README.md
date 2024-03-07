# How to shorten Powershell Current Path

Run powershell as Administrator, then type
Test-Path $Profile

if it returns false then you have to create powershell profile

to create powershell profile type
New-Item -Path $Profile -Type File -Force

now type
notepad $Profile

in notepad enter
function prompt {
	$p = -path
	"$p> "
}
save and exit

then type the following in powershell
Set-ExecutionPolicy RemoteSigned
type
Y
you are good to go
