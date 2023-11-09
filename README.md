# tr_bolgeler
Türkiye'nin 7 Bölgesi GeoJSON Formatında ve LeafletJS örnek uygulama

Türkiye'nin 7 Bölgesi GeoJSON Formatında ve LeafletJS örnek uygulama

<!DOCTYPE html>
<html>
<body>

<h1>Türkiye'nin 7 Bölgesi GeoJSON Formatında ve LeafletJS örnek uygulama</h1>
<p>Türkiye'nin 7 bölgesi Cihad TURHAN'ın hazırladığı "<a href="https://github.com/cihadturhan/tr-geojson" target="_blank" title="Türkiye GeoJSON haritası">Türkiye GeoJSON haritası</a>" verileri kullanılarak hazırlandı.</p>

<div id="leaflet_map" style="width: 100%;height: 500px"></div>

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY=" crossorigin=""/>
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js" integrity="sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo=" crossorigin=""></script>

<script src="bolgeler_v1/akdeniz1.js"></script>

<script>
	var myIcon = L.icon({
		iconUrl: 'https://leafletjs.com/examples/custom-icons/leaf-green.png',
	});
	
	const map = L.map('leaflet_map').setView([39.136818, 35.087120], 6);

	const tiles = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
		maxZoom: 18,
		attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
	}).addTo(map);

	L.geoJSON([akdeniz1]).addTo(map);
</script>

</body>
</html>
