---
title: Generar un cuadro de diálogo para seleccionar un filtro
description: Generar un cuadro de diálogo para seleccionar un filtro
ms.assetid: 4cbb9276-6ce6-4cf4-a000-2b4f9ac42b31
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (Administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- acmFilterChoose función)
- Administrador de compresión de audio (ACM), seleccionar filtros
- ACM (Administrador de compresión de audio), seleccionar filtros
- Ejemplos de ACM, seleccionar filtros
- selección de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87225c1aebf2a06c738a1b48b03b94ed81bf6c2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676141"
---
# <a name="producing-a-dialog-box-for-selecting-a-filter"></a><span data-ttu-id="df515-112">Generar un cuadro de diálogo para seleccionar un filtro</span><span class="sxs-lookup"><span data-stu-id="df515-112">Producing a Dialog Box for Selecting a Filter</span></span>

<span data-ttu-id="df515-113">Una aplicación puede permitir a los usuarios seleccionar una operación de filtro arbitraria y aplicarla a los datos de audio de una onda.</span><span class="sxs-lookup"><span data-stu-id="df515-113">An application can allow users to select an arbitrary filter operation and apply it to waveform-audio data.</span></span> <span data-ttu-id="df515-114">En el ejemplo siguiente, la aplicación asigna un búfer para contener el filtro y, a continuación, usa la función [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) para seleccionar el filtro.</span><span class="sxs-lookup"><span data-stu-id="df515-114">In the following example, the application allocates a buffer to hold the filter and then uses the [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) function to select the filter.</span></span> <span data-ttu-id="df515-115">Se debe llamar a las funciones de este ejemplo con el filtro o la etiqueta de filtro adecuados.</span><span class="sxs-lookup"><span data-stu-id="df515-115">The functions in this example must be called with the appropriate filter or filter tag.</span></span>


```C++
MMRESULT        mmr; 
ACMFILTERCHOOSE afc; 
PWAVEFILTER     pwfltr; 
DWORD           cbwfltr; 
 
// Determine the maximum size required for any valid filter 
// for which the ACM has a driver installed and enabled. 
mmr = acmMetrics(NULL, ACM_METRIC_MAX_SIZE_FILTER, &cbwfltr); 
if (MMSYSERR_NOERROR != mmr) { 
 
    // The ACM probably has no drivers installed and 
    // enabled for filter operations. 
    return (mmr); 
} 
 
// Dynamically allocate a structure large enough to hold the 
// maximum sized filter enabled in the system. 
pwfltr = (PWAVEFILTER)LocalAlloc(LPTR, (UINT)cbwfltr); 
if (NULL == pwfltr) { 
    return (MMSYSERR_NOMEM); 
} 
 
// Initialize the ACMFILTERCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfltr      = pwfltr;           // wfltr to receive selection 
afc.cbwfltr     = cbwfltr;          // size of wfltr buffer 
afc.pszTitle    = TEXT("Any Filter Selection"); 
 
// Call the ACM to bring up the filter-selection dialog box. 
mmr = acmFilterChoose(&afc); 
if (MMSYSERR_NOERROR == mmr) { 
    // The user selected a valid filter. The pwfltr buffer, 
    // allocated above, contains the complete filter description. 
} 
 
// Clean up and exit. 
LocalFree((HLOCAL)pwfltr); 
return (mmr); 
 
```



 

 




