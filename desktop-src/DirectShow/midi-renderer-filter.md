---
description: El filtro representador de MIDI representa los datos DE MIDI del filtro del analizador de MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro de representador DE MIDI (Windows.devices.midi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909413"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="48ea7-103">Filtro de representador de MIDI</span><span class="sxs-lookup"><span data-stu-id="48ea7-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="48ea7-104">El filtro representador de MIDI representa los datos DE MIDI del filtro [del analizador de MIDI.](midi-parser-filter.md)</span><span class="sxs-lookup"><span data-stu-id="48ea7-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



| <span data-ttu-id="48ea7-105">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="48ea7-105">Label</span></span> | <span data-ttu-id="48ea7-106">Value</span><span class="sxs-lookup"><span data-stu-id="48ea7-106">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48ea7-107">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="48ea7-107">Filter Interfaces</span></span>                        | <span data-ttu-id="48ea7-108">[**IAMClockVicee,**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave) [**IAMDirectSound,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="48ea7-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="48ea7-109">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="48ea7-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="48ea7-110">MEDIATYPE \_ Midi, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="48ea7-110">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="48ea7-111">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="48ea7-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="48ea7-112">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="48ea7-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="48ea7-113">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="48ea7-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="48ea7-114">No aplicable</span><span class="sxs-lookup"><span data-stu-id="48ea7-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="48ea7-115">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="48ea7-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="48ea7-116">No aplicable</span><span class="sxs-lookup"><span data-stu-id="48ea7-116">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="48ea7-117">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="48ea7-117">Filter CLSID</span></span>                             | <span data-ttu-id="48ea7-118">CLSID \_ AVIMIDIRender</span><span class="sxs-lookup"><span data-stu-id="48ea7-118">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="48ea7-119">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="48ea7-119">Property Page CLSID</span></span>                      | <span data-ttu-id="48ea7-120">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="48ea7-120">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="48ea7-121">Executable</span><span class="sxs-lookup"><span data-stu-id="48ea7-121">Executable</span></span>                               | <span data-ttu-id="48ea7-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="48ea7-122">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="48ea7-123">Mérito</span><span class="sxs-lookup"><span data-stu-id="48ea7-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="48ea7-124">MERIT \_ PREFERRED</span><span class="sxs-lookup"><span data-stu-id="48ea7-124">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="48ea7-125">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="48ea7-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="48ea7-126">CLSID \_ MidiRendererCategory</span><span class="sxs-lookup"><span data-stu-id="48ea7-126">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="48ea7-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48ea7-127">Remarks</span></span>

<span data-ttu-id="48ea7-128">El GUID del tipo de formato **es NULL,** pero el bloque de formato contiene la siguiente estructura:</span><span class="sxs-lookup"><span data-stu-id="48ea7-128">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="48ea7-129">El **miembro dwDivision** especifica la división de tiempo del archivo.</span><span class="sxs-lookup"><span data-stu-id="48ea7-129">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="48ea7-130">La división de tiempo se da en el encabezado de cualquier archivo MIDI estándar (SMF), en el `MThd` fragmento.</span><span class="sxs-lookup"><span data-stu-id="48ea7-130">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="48ea7-131">El representador de MIDI establece esta propiedad en el flujo de datos de MIDI mediante una llamada a **la función midiStreamProperty.**</span><span class="sxs-lookup"><span data-stu-id="48ea7-131">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="48ea7-132">Los ejemplos del filtro analizador DE MIDI contienen un segundo de datos DE MIDI.</span><span class="sxs-lookup"><span data-stu-id="48ea7-132">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="48ea7-133">El representador de MIDI usa **la función midiStreamOut** para representar los datos de MIDI.</span><span class="sxs-lookup"><span data-stu-id="48ea7-133">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="48ea7-134">Cada ejemplo es un punto de sincronización: el inicio del búfer contiene todos los comandos necesarios para establecer el estado correcto para representar ese búfer.</span><span class="sxs-lookup"><span data-stu-id="48ea7-134">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="48ea7-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48ea7-135">Requirements</span></span>



| <span data-ttu-id="48ea7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="48ea7-136">Requirement</span></span> | <span data-ttu-id="48ea7-137">Value</span><span class="sxs-lookup"><span data-stu-id="48ea7-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48ea7-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48ea7-138">Header</span></span><br/> | <dl> <span data-ttu-id="48ea7-139"><dt>Windows.devices.midi.h</dt></span><span class="sxs-lookup"><span data-stu-id="48ea7-139"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48ea7-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="48ea7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48ea7-141">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="48ea7-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




