---
title: Reproducir recursos de WAVE
description: Reproducir recursos de WAVE
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- audio de onda, reproducir recursos de onda
- audio auxiliar, reproducir recursos de onda
- reproducir recursos de WAVE
- Función PlaySound, reproducir recursos de WAVE
- sndPlaySound función)
- Función PlaySound, en comparación con la función sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9678c18e09b12ee1e8d8215d0841cbdaba0ac9c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487695"
---
# <a name="playing-wave-resources"></a>Reproducir recursos de WAVE

Puede utilizar la función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) para reproducir un sonido que se almacena como un recurso. Aunque esto también se puede hacer con la función [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) , **sndPlaySound** requiere que encuentre, cargue, bloquee, desbloquee y libere el recurso; **PlaySound** consigue todo esto con una sola línea de código.

## <a name="playsound-example"></a>Ejemplo de PlaySound


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>Ejemplo de sndPlaySound

La \_ marca de memoria SND indica que el parámetro *lpszSoundName* es un puntero a una imagen en memoria del archivo de onda. Para incluir un archivo de onda como un recurso en una aplicación, agregue la entrada siguiente al script de recursos de la aplicación (. RC).


```C++
soundName WAVE c:\sounds\bells.wav 
```



El nombre *soundName* es un marcador de posición para un nombre que se proporciona para hacer referencia a este recurso de onda. Los recursos de WAVE se cargan y se obtiene acceso a ellos igual que otros recursos de Windows definidos por la aplicación. La función PlayResource del siguiente ejemplo reproduce un recurso de onda especificado.


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



Para reproducir un recurso de onda mediante esta función, pase a la función un puntero a una cadena que contiene el nombre del recurso, tal como se muestra en el ejemplo siguiente.


```C++
PlayResource("soundName"); 
```



 

 