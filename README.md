# Rest_API_MedRec
Rest API for E-Health: Smart Card for medical record

# A. How to Run
1. Install Node js, add node js to environment PATH
2. Reboot computer
3. Extract zip to ***dir*
4. Open command prompt, change directory to dir via: cd ***dir*
5. start the server by : npm start
6. id it works, it will give you: "connect to DB moongoose compass"

# B. REQUEST FORMAT EXAMPLE
notes: the other reuest format can be seen from ..\routes\patient.js
1. **POST** Data diri pasien
    **Url**: http://localhost:4000/patient/datadiri
    **Body Example: 
    {
    "identifier" : {
        "value" : "123457"
    },
    "name" : {
        "given" : "Nama Orang"
    },
    "telecom" : {
        "value" : "0808202082",
        "use" : "mobile"
    },
    "gender" : "Perempuan",
    "birthDate" : "1996-05-23",
    "address" : {
        "alamat" : "jl melati",
        "kelurahan" : ["32.01.01.1001", "Pondok Rajeg"],
        "kecamatan" : ["32.01.01", "Cibinong"],
        "kabupaten" : ["32.01", "KAB. BOGOR"],
        "provinsi" :   ["32", "JAWA BARAT"]
    },
    "martialStatus" : "Belum Kawin",
    "contact" : {
        "relationship" : "Ibu",
        "name" : {
            "given" : "Nama Ibu"
        },
        "telecom" : {
            "value" : "0808202082"
        },
        "address" : {
            "alamat" : "jl melati",
            "kelurahan" : ["32.01.01.1001", "Pondok Rajeg"],
            "kecamatan" : ["32.01.01", "Cibinong"],
            "kabupaten" : ["32.01", "KAB. BOGOR"],
            "provinsi" :   ["32", "JAWA BARAT"]
        }
    },
    "managingOrganization" : "RSUD Bogor",
    "generalPractitioner" : "Nama Petugas Medis"
    }
    
2. **GET** Data diri pasien: to get all data diri pasien
    **Url**: http://localhost:4000/patient/datadiri/
    **Body Example: <no body>

2. **POST** Rekam Medis Statis: to get store rekam medis to server
    **Url**: http://localhost:4000/patient/datastatis
    **Body Example:
    {
			"identifier":{
				"type":"DATA STATIS",
				"value":"000003"
			},
    		"alergi" : "alergi 0001",
   			"GolonganDarah" : "A+",
        	"RiwayatOperasi" : "Riwayat Operasi",
        	"RiwayatRawatRS" : "Riwayat Rawat RS",
        	"RiwayatPenyakitKronis" : "Riwayat Penyakit Kronis",
        	"RiwayatPenyakitBawaan" : "Riwayat Penyakit Bawaan",
        	"FaktorResiko" : "Faktor Resiko"
    }

