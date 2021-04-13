---
title: Generar un cuadro de diálogo para seleccionar un tipo de formato específico
description: Generar un cuadro de diálogo para seleccionar un tipo de formato específico
ms.assetid: e454f9d6-5cbf-4e1b-937e-771cf1dd38ba
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (Administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- acmFormatChoose función)
- Administrador de compresión de audio (ACM), seleccionar tipos de formato
- ACM (Administrador de compresión de audio), seleccionar tipos de formato
- Ejemplos de ACM, seleccionar tipos de formato
- seleccionar tipos de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfc5d73d1b03f22923e6001d65898c05e2bd853e
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/27/2020
ms.locfileid: "104358739"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a><span data-ttu-id="abb56-112">Generar un cuadro de diálogo para seleccionar un tipo de formato específico</span><span class="sxs-lookup"><span data-stu-id="abb56-112">Producing a Dialog Box for Selecting a Specific Type of Format</span></span>

<span data-ttu-id="abb56-113">Es posible que desee que una aplicación permita al usuario seleccionar un formato de una lista restringida de formatos en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="abb56-113">You might want an application to allow the user to select a format from a restricted list of formats in a dialog box.</span></span> <span data-ttu-id="abb56-114">Las restricciones pueden limitar el número de canales, la velocidad de muestreo, la etiqueta de formato de audio de forma de onda o el número de bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="abb56-114">Restrictions might limit the number of channels, the sampling rate, the waveform-audio format tag, or the number of bits per sample.</span></span> <span data-ttu-id="abb56-115">En todos estos casos, puede generar la lista con la función [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , estableciendo los miembros **fdwEnum** y **pwfxEnum** de la estructura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="abb56-115">In all of these cases, you can generate the list by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, setting the **fdwEnum** and **pwfxEnum** members of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span> <span data-ttu-id="abb56-116">El ejemplo siguiente ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="abb56-116">The following example illustrates this process.</span></span>


```C++
MMRESULT            mmr; 
ACMFORMATCHOOSE     afc; 
WAVEFORMATEX        wfxSelection; 
WAVEFORMATEX        wfxEnum; 
 
// Initialize the ACMFORMATCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfx        = &wfxSelection;    // wfx to receive selection 
afc.cbwfx       = sizeof(wfxSelection); 
afc.pszTitle    = TEXT("16 Bit PCM Selection"); 
 
//  Request that all 16-bit PCM formats be displayed for the user 
//  to select from. 
memset(&wfxEnum, 0, sizeof(wfxEnum)); 
wfxEnum.wFormatTag = WAVE_FORMAT_PCM; 
wfxEnum.wBitsPerSample = 16; 
afc.fdwEnum = ACM_FORMATENUMF_WFORMATTAG | 
    ACM_FORMATENUMF_WBITSPERSAMPLE; 
afc.pwfxEnum = &wfxEnum; 
mmr = acmFormatChoose(&afc); 
if ((MMSYSERR_NOERROR != mmr) && (ACMERR_CANCELED != mmr)) 
{ 
    // There was a fatal error in bringing up the list 
    // dialog box (probably invalid input parameters). 
} 
 
```



 

 




