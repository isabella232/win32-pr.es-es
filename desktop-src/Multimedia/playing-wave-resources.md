---
title: Reproducción de recursos de WAVE
description: Reproducción de recursos de WAVE
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- audio de forma de onda, reproducir recursos wave
- audio auxiliar, reproducir recursos wave
- reproducir recursos de WAVE
- Función PlaySound, reproducir recursos wave
- Función sndPlaySound
- Función PlaySound, en comparación con la función sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9678c18e09b12ee1e8d8215d0841cbdaba0ac9c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371318"
---
# <a name="playing-wave-resources"></a>Reproducción de recursos de WAVE

Puede usar la función [**Play Sound**](/previous-versions//dd743680(v=vs.85)) para reproducir un sonido que se almacena como un recurso. Aunque esto también es posible mediante la función [**sndPlaySound,**](/previous-versions//dd798676(v=vs.85)) **sndPlaySound** requiere que encuentre, cargue, bloquee, desbloquee y libre el recurso. **PlaySound** consigue todo esto con una sola línea de código.

## <a name="playsound-example"></a>Ejemplo de PlaySound


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>Ejemplo de sndPlaySound

La marca MEMORY de SND indica que el parámetro \_ *lpszSoundName* es un puntero a una imagen en memoria del archivo WAVE. Para incluir un archivo WAVE como un recurso en una aplicación, agregue la siguiente entrada al script de recursos de la aplicación (. RC).


```C++
soundName WAVE c:\sounds\bells.wav 
```



El nombre *soundName es* un marcador de posición de un nombre que se proporciona para hacer referencia a este recurso WAVE. Los recursos wave se cargan y se accede al igual que otros recursos de Windows definidos por la aplicación. La función PlayResource del ejemplo siguiente reproduce un recurso WAVE especificado.


```C++
BOOL PlayResource(LPSTR lpName) 
{ 
    BOOL bRtn; 
    LPSTR lpRes; 
    HANDLE hResInfo, hRes; 
 
    // Find the WAVE resource. 
 
    hResInfo = FindResource(hInst, lpName, "WAVE"); 
    if (hResInfo == NULL) 
        return FALSE; 
 
    // Load the WAVE resource. 
 
    hRes = LoadResource(hInst, hResInfo); 
    if (hRes == NULL) 
        return FALSE; 
 
    // Lock the WAVE resource and play it. 
 
    lpRes = LockResource(hRes); 
    if (lpRes != NULL) { 
        bRtn = sndPlaySound(lpRes, SND_MEMORY | SND_SYNC | 
            SND_NODEFAULT); 
        UnlockResource(hRes); 
    } 
    else 
        bRtn = 0; 
 
    // Free the WAVE resource and return success or failure. 
 
    FreeResource(hRes); 
    return bRtn; 
} 
```



Para reproducir un recurso WAVE mediante esta función, pase a la función un puntero a una cadena que contenga el nombre del recurso, como se muestra en el ejemplo siguiente.


```C++
PlayResource("soundName"); 
```



 

 