# Sample for [xslt-service](https://github.com/FilipJirsak/xslt-service)

Usage: 

```
curl --request POST --url http://localhost:8080/financni-urad --header 'Content-Type: application/json' --data @input.json
```

Sample input file:
```
{
    "zadatel": {
        "jmeno": "Tomáš",
        "prijmeni": "Novák",
        "rodneCislo": "010101/3000",
        "email": "tnovak@seznam.cz",
        "telefon": "326123456",
        "adresa": {
            "radky": ["Sokolovská 1"],
            "obec": "Čelákovice",
            "psc": "25088"
            }
    },
    "urad": {
        "adresa": {
            "radky": [
                "Finanční úřad pro Středočeský kraj",
                "Boleslavská 31"
            ],
            "obec": "Brandýs n. L. – Stará Boleslav",
            "psc": "25002"
        },
        "email": "podatelna2105@fs.mfcr.cz",
        "datovaSchranka": "6sxny3p",
        "telefon": "326910302"
	},
	"ucel": [
		"jednání u Úřadu práce ČR (dle zákona č. 435/2004 Sb., o zaměstnanosti, v platném znění),",
		"jednání u bankovní instituce,",
		"pro klid v duši."
	],
	"odpoved": {
		"trvaleBydliste": null,
		"datovaSchranka": "abcdefg"
	},
	"podpis": {
		"misto": "Praze",
		"datum": "2021-02-22",
		"jmeno": "Tomáš",
		"prijmeni": "Novák"
	}
}'
```

V objektu `odpoved` může být také null property `osobne` nebo stringové property `email` nebo `datovaSchranka`. 
