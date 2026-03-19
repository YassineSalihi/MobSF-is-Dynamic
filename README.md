# Analyse Dynamique Mobile avec MobSF

## Création de l’émulateur AVD sans Play Store

![émulateur](https://github.com/user-attachments/assets/50315391-5d5d-46de-a8dc-0c28e6821606)

## Cloner MobSF pour utiliser les scripts AVD officiels

On Ouvre un terminal et on tape :

~~~sh
git clone https://github.com/MobSF/Mobile-Security-Framework-MobSF.git
cd Mobile-Security-Framework-MobSF
~~~

![pic of cmds](https://github.com/user-attachments/assets/9f80ed9d-a188-44d6-86ff-f579b690a1a3)

## Lancement de l’émulateur avec le script MobSF (rooté & prêt pour l’analyse)

On lance le script pour savoir notre avds:

~~~sh
  ./scripts/start_avd.sh 
~~~

![avds](https://github.com/user-attachments/assets/299d3ce3-9ff8-460f-8501-816fd8fd7686)

On lance le script pour allumer l'émulateur:

~~~sh
  ./scripts/start_avd.sh Pixel_4_XL_2
~~~

![turn on](https://github.com/user-attachments/assets/c0a2b97e-98c9-47d0-8fd0-976c72396618)

Vérification :

![verification](https://github.com/user-attachments/assets/78ff3775-dbf5-4efd-a976-3263690f6a58)

## Installation et lancement de MobSF via Docker

On lance la commande docker :

~~~sh
docker run -it --rm \
  -p 8000:8000 \
  -e MOBSF_ANALYZER_IDENTIFIER=emulator-5554 \
  opensecurity/mobile-security-framework-mobsf:latest
~~~

On voit dans le lien ***<http://127.0.0.1/8000>*** :

![login page](https://github.com/user-attachments/assets/85c6ba0f-5c30-4ca8-983a-3fe0af974261)

![upload page](https://github.com/user-attachments/assets/c03b4b3e-6f11-4b5a-bd23-0b788149b95c)

## Analyse Statique + Dynamique de DIVA

 On choisit notre apk:

![upload apk](https://github.com/user-attachments/assets/a759fa1d-88af-4b36-af06-c8a020a3385a)

Voilà la fin des analyses statiques :

![info sur diva](https://github.com/user-attachments/assets/3723d544-1b34-40e9-92b1-89cc21f4d78f)

> ### 🔴 CRITICAL PROBLEM
>
> MobSF wasn't able to connect with emulator-5554.
> **Fix : Switch to genymotion.**

### Voilà genymotion

![installation](https://github.com/user-attachments/assets/c5dd06e0-ee37-4bbe-ae65-dcceaf423ff6)

### Emulateur + Interface

![InterfacePlusEmu](https://github.com/user-attachments/assets/8720ac79-c45f-4b3e-9a40-fd22a9c205b5)

### Commencer MainActivity

![start_main](https://github.com/user-attachments/assets/6d9af1cc-e254-45df-ac10-0d44424966b0)

On fait le Challenge de "Hardcoded issue" :

<https://github.com/user-attachments/assets/cf2df5e0-6887-41fb-907b-05f7c78d34be>
