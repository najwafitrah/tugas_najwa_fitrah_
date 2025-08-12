<!DOCTYPE html>
<html>
<head>
    <title>Formulir Lengkap</title>
    <style>
        body {
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
            padding: 20px;
        }
        h2 {
            color: #dd0000;
            text-align: center;
            margin-bottom: 20px;
        }
        .form-container {
            background-color: #ffffff;
            border: 1px solid #ccc;
            padding: 20px;
            border-radius: 8px;
        }
        legend {
            color: #f6ff00;
            font-weight: bold;
            font-size: 18px;
        }
        label {
            display: block;
            margin-top: 15px;
            font-weight: bold;
            color: #333;
        }
        input[type="text"], input[type="password"], textarea, select {
            width: 95%;
            padding: 8px;
            margin-top: 5px;
            border: 1px solid #949494;
            border-radius: 4px;
        }
        .button-group {
            margin-top: 20px;
        }
        .button-group input, .button-group button {
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-right: 10px;
        }
        input[type="submit"] {
            background-color: #4CAF50;
            color: white;
        }
        button[type="reset"] {
            background-color: #f44336;
            color: white;
        }
        img, video {
            display: block;
            margin-top: 10px;
            max-width: 300px;
            border-radius: 6px;
        }
    </style>
</head>
<body>
    <h2>
        <marquee behavior="alternate" scrollamount="10">
            Demo Membuat Form Lengkap
        </marquee>
    </h2>

    <div class="form-container">
        <form>
            <fieldset>
                <legend>Formulir Pendaftaran Lengkap</legend>

                <input type="hidden" name="user_id" value="12345">

                <label for="nama">Nama</label>
                <input type="text" id="nama" name="txtNama" size="30" />

                <label for="password">Password</label>
                <input type="password" id="password" name="txtPassword" size="30" placeholder="Masukkan password Anda" />

                <label for="alamat">Alamat</label>
                <textarea id="alamat" name="Alamat" rows="4"></textarea>

                <label for="telepon">Telepon</label>
                <input type="text" id="telepon" name="txtTelepon" size="20" />

                <label for="Jurusan">Asal Jurusan</label>
                <select id="Jurusan" name="selectJurusan">
                    <option value="">-- Pilih Jurusan --</option>
                    <option value="tkj">TKJ</option>
                    <option value="rpl">RPL</option>
                    <option value="mplb">MPLB</option>
                    <option value="pms">PMS</option>
                </select>

                <label>Jenis Kelamin</label>
                <input type="radio" name="gender" value="pria" id="pria"><label for="pria" style="display:inline;">Pria</label>
                <input type="radio" name="gender" value="wanita" id="wanita"><label for="wanita" style="display:inline;">Wanita</label>

                <label>KELAS? (Checkbox)</label>
                <input type="checkbox" name="kelas" value="1" id="1"><label for="1" style="display:inline;">1</label><br>
                <input type="checkbox" name="kelas" value="2" id="2"><label for="2" style="display:inline;">2</label><br>
                <input type="checkbox" name="kelas" value="3" id="3"><label for="3" style="display:inline;">3</label>

                <label for="berkas">Unggah foto (File)</label>
                <input type="file" id="berkas" name="fileCV" accept="image/*" onchange="previewImage(event)">
                <img id="previewFoto" src="#" alt="Preview Foto" style="display:none;">

                <label for="videoFile">Unggah video</label>
                <input type="file" id="videoFile" name="fileVideo" accept="video/*" onchange="previewVideo(event)">
                <video id="previewVideo" controls style="display:none;"></video>

                <div class="button-group">
                    <input type="submit" value="Submit" />
                    <button type="reset" onclick="resetPreview()">Reset</button>
                </div>
            </fieldset>
        </form>
    </div>

    <script>
        function previewImage(event) {
            const foto = document.getElementById('previewFoto');
            foto.src = URL.createObjectURL(event.target.files[0]);
            foto.style.display = 'block';
        }
        function previewVideo(event) {
            const video = document.getElementById('previewVideo');
            video.src = URL.createObjectURL(event.target.files[0]);
            video.style.display = 'block';
        }
        function resetPreview() {
            document.getElementById('previewFoto').style.display = 'none';
            document.getElementById('previewVideo').style.display = 'none';
        }
    </script>
</body>
</html>

