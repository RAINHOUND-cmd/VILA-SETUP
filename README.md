# VILA-SETUP
Script contained within a .txt file that allows NVIDIA's VLM, VILA, to be set up for a single GPU system and perform a dry-run

To use the custom script you must first create a new file that contains the script commands:
1. Open WSL
2. Use a text editor such as nano to create a new script file. Ex: nano setupscript.sh
3. Paste the script contents into the editor
4. For nano: Save(Ctrl-O) --> hit enter --> Exit(Ctrl-X)

After saving the file give it execute permissions: 
1. chmod +x myscript.sh

You may now run the script from your current directory
./setupscript.sh
