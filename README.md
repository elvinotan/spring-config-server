# spring-config-server
Spring Cloud Config adalah salah satu feature dari Netflix yang memungkinkan configurasi di simpan di dalam server ini. Konfigurasi yang di simpan di server ini bukan hanya untuk server ini, tp bisa juga untuk semua server yang ada. Cara kerja dari Spring Config Server ini adalah pada saat server ini booting dia akan mencari bootstrap.properties yang memiliki property letak dari konfigurasi

# dependencies
Config Server

# how to
1. Tambahkan <code>@EnableConfigServer</code> pada SpringBootApplication class, dgn konfigursi ini menandakan bila server ini akan di gunakan sebagi config server, dan akan error bila property <code>spring.cloud.config.server.git.uri</code> tidak tersedia.
2. Buatlah bootstrap.properties selevel dengan application.properties. lalu isi dengan nilai <code>spring.cloud.config.server.git.uri=https://github.com/elvinotan/config</code>. 
Konfigurasi ini menandakan pada saat server config ini hidup, please ambil konfigurasi di alamat <code>https://github.com/elvinotan/config</code>
3. Untuk Setup sisi server selesai, next please refer to spring-config-client
