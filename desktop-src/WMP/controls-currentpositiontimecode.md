---
title: Controls. currentPositionTimecode
description: La propiedad currentPositionTimecode especifica o recupera la posición actual en el elemento multimedia actual mediante un formato de código de tiempo. Esta propiedad admite actualmente código de tiempo SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Media Player de Windows Controls. currentPositionTimecode
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698653"
---
# <a name="controlscurrentpositiontimecode"></a><span data-ttu-id="96f76-105">Controls. currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="96f76-105">Controls.currentPositionTimecode</span></span>

<span data-ttu-id="96f76-106">La propiedad **currentPositionTimecode** especifica o recupera la posición actual en el elemento multimedia actual mediante un formato de código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="96f76-106">The **currentPositionTimecode** property specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="96f76-107">Esta propiedad admite actualmente código de tiempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="96f76-107">This property currently supports SMPTE time code.</span></span>

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a><span data-ttu-id="96f76-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="96f76-108">Possible Values</span></span>

<span data-ttu-id="96f76-109">Esta propiedad es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="96f76-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="96f76-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96f76-110">Remarks</span></span>

<span data-ttu-id="96f76-111">El código de tiempo SMPTE proporciona una forma estándar de identificar un fotograma de vídeo individual, que es útil para sincronizar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="96f76-111">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="96f76-112">Si un archivo multimedia digital admite código de tiempo SMPTE, Windows Media Player puede recuperar la información de posición del código de tiempo actual o buscar un fotograma de vídeo identificado por una **cadena** de código de tiempo determinada.</span><span class="sxs-lookup"><span data-stu-id="96f76-112">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code **String**.</span></span>

<span data-ttu-id="96f76-113">El código de tiempo SMPTE identifica un fotograma determinado por el número de horas, minutos, segundos y fotogramas que lo separan de un marco de referencia determinado, el marco designado como tiempo cero.</span><span class="sxs-lookup"><span data-stu-id="96f76-113">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="96f76-114">Normalmente, el marco de cero de tiempo es el inicio del archivo y un valor de código de tiempo de SMPTE determinado representa el tiempo transcurrido desde el inicio del archivo.</span><span class="sxs-lookup"><span data-stu-id="96f76-114">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="96f76-115">La **cadena** de código de tiempo está en el intervalo de formato \[  \] *HH*:*mm*:*SS*.*FF* donde \[ *Range* \] representa el intervalo, *HH* representa las horas, *mm* representa los minutos, *SS* representa los segundos y *FF* representa los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="96f76-115">The time code **String** is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, *hh* represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="96f76-116">Al especificar un valor mediante **currentPositionTimecode**, debe incluir los ocho dígitos usando ceros como marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="96f76-116">When specifying a value using **currentPositionTimecode**, you must include all eight digits using zeros as placeholders.</span></span>

<span data-ttu-id="96f76-117">El \[  \] especificador de intervalo se corresponde con el miembro **wRange** de la estructura de datos de la **extensión de código de \_ tiempo \_ \_ WMT** del formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="96f76-117">The \[*range*\] specifier corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="96f76-118">Para obtener más información acerca de los intervalos de código de tiempo, vea el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="96f76-118">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="96f76-119">Solo se admite la especificación y recuperación de **currentPositionTimecode** para los archivos que contienen información de código de tiempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="96f76-119">Specifying and retrieving **currentPositionTimecode** is only supported for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="96f76-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="96f76-120">Examples</span></span>

<span data-ttu-id="96f76-121">En el ejemplo de código siguiente se especifica **currentPositionTimecode** como 1 hora, cero minutos, 30 segundos y 5 fotogramas.</span><span class="sxs-lookup"><span data-stu-id="96f76-121">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="96f76-122">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="96f76-122">The **Player** object was created with ID = "Player".</span></span>


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a><span data-ttu-id="96f76-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96f76-123">Requirements</span></span>



| <span data-ttu-id="96f76-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="96f76-124">Requirement</span></span> | <span data-ttu-id="96f76-125">Value</span><span class="sxs-lookup"><span data-stu-id="96f76-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96f76-126">Versión</span><span class="sxs-lookup"><span data-stu-id="96f76-126">Version</span></span><br/> | <span data-ttu-id="96f76-127">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="96f76-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="96f76-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96f76-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="96f76-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96f76-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96f76-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="96f76-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f76-131">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="96f76-131">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





