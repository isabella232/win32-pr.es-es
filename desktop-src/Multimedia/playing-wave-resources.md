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
# <a name="playing-wave-resources"></a><span data-ttu-id="d41e4-109">Reproducir recursos de WAVE</span><span class="sxs-lookup"><span data-stu-id="d41e4-109">Playing WAVE Resources</span></span>

<span data-ttu-id="d41e4-110">Puede utilizar la función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) para reproducir un sonido que se almacena como un recurso.</span><span class="sxs-lookup"><span data-stu-id="d41e4-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play a sound that is stored as a resource.</span></span> <span data-ttu-id="d41e4-111">Aunque esto también se puede hacer con la función [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) , **sndPlaySound** requiere que encuentre, cargue, bloquee, desbloquee y libere el recurso; **PlaySound** consigue todo esto con una sola línea de código.</span><span class="sxs-lookup"><span data-stu-id="d41e4-111">Although this is also possible using the [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function, **sndPlaySound** requires that you find, load, lock, unlock, and free the resource; **PlaySound** achieves all of this with a single line of code.</span></span>

## <a name="playsound-example"></a><span data-ttu-id="d41e4-112">Ejemplo de PlaySound</span><span class="sxs-lookup"><span data-stu-id="d41e4-112">PlaySound Example</span></span>


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a><span data-ttu-id="d41e4-113">Ejemplo de sndPlaySound</span><span class="sxs-lookup"><span data-stu-id="d41e4-113">sndPlaySound Example</span></span>

<span data-ttu-id="d41e4-114">La \_ marca de memoria SND indica que el parámetro *lpszSoundName* es un puntero a una imagen en memoria del archivo de onda.</span><span class="sxs-lookup"><span data-stu-id="d41e4-114">The SND\_MEMORY flag indicates that the *lpszSoundName* parameter is a pointer to an in-memory image of the WAVE file.</span></span> <span data-ttu-id="d41e4-115">Para incluir un archivo de onda como un recurso en una aplicación, agregue la entrada siguiente al script de recursos de la aplicación (. RC).</span><span class="sxs-lookup"><span data-stu-id="d41e4-115">To include a WAVE file as a resource in an application, add the following entry to the application's resource script (.RC) file.</span></span>


```C++
soundName WAVE c:\sounds\bells.wav 
```



<span data-ttu-id="d41e4-116">El nombre *soundName* es un marcador de posición para un nombre que se proporciona para hacer referencia a este recurso de onda.</span><span class="sxs-lookup"><span data-stu-id="d41e4-116">The name *soundName* is a placeholder for a name that you supply to refer to this WAVE resource.</span></span> <span data-ttu-id="d41e4-117">Los recursos de WAVE se cargan y se obtiene acceso a ellos igual que otros recursos de Windows definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d41e4-117">WAVE resources are loaded and accessed just like other application-defined Windows resources.</span></span> <span data-ttu-id="d41e4-118">La función PlayResource del siguiente ejemplo reproduce un recurso de onda especificado.</span><span class="sxs-lookup"><span data-stu-id="d41e4-118">The PlayResource function in the following example plays a specified WAVE resource.</span></span>


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



<span data-ttu-id="d41e4-119">Para reproducir un recurso de onda mediante esta función, pase a la función un puntero a una cadena que contiene el nombre del recurso, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d41e4-119">To play a WAVE resource by using this function, pass to the function a pointer to a string containing the name of the resource, as shown in the following example.</span></span>


```C++
PlayResource("soundName"); 
```



 

 