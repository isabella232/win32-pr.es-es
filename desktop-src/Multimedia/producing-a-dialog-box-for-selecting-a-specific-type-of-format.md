---
title: Generar un cuadro de diálogo para seleccionar un tipo específico de formato
description: Generar un cuadro de diálogo para seleccionar un tipo específico de formato
ms.assetid: e454f9d6-5cbf-4e1b-937e-771cf1dd38ba
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- Función acmFormatChoose
- Administrador de compresión de audio (ACM), selección de tipos de formato
- ACM (administrador de compresión de audio), selección de tipos de formato
- Ejemplos de ACM, selección de tipos de formato
- seleccionar tipos de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f25f7b196fcb9462a3b61dd8e351ed75276c7df7bf46cec233dd8eac7deda5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037655"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a>Generar un cuadro de diálogo para seleccionar un tipo específico de formato

Es posible que desee que una aplicación permita al usuario seleccionar un formato de una lista restringida de formatos en un cuadro de diálogo. Las restricciones pueden limitar el número de canales, la velocidad de muestreo, la etiqueta de formato de audio de forma de onda o el número de bits por muestra. En todos estos casos, puede generar la lista mediante la función [**acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) estableciendo los **miembros fdwEnum** y **pwfxEnum** de la estructura [**ACMFORMATCHOOSE.**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) El ejemplo siguiente ilustra este proceso.


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



 

 




