Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.50.55"
  config.vm.synced_folder ".", "/examen-david-fdz-suco"
  
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    echo "-- Insertar datos en la tabla 'menu'" > /home/vagrant/datos_menu.sql
echo "INSERT INTO gestion_restaurante.menu(nombre, descripcion, precio, categoria) VALUES" >> /home/vagrant/datos_menu.sql
echo "('Ensalada Mixta', 'Ensalada lechuga, tomate, cebolla', '15', 'ensaladas')," >> /home/vagrant/datos_menu.sql
echo "('Pasta Carbonara', 'espaguetis, huevo, guancciale, parmesano', '18', 'pastas')," >> /home/vagrant/datos_menu.sql
echo "('Rissotto de boletus', 'arroz, mantequilla, boletus', '20', 'arroces');" >> /home/vagrant/datos_menu.sql



  SHELL

 
 
end