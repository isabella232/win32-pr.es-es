---
description: El filtro de representador MIDI representa datos MIDI del filtro de analizador MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtro de representador MIDI (Windows. Devices. MIDI. h)
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
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690778"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="37b58-103">Filtro de representador MIDI</span><span class="sxs-lookup"><span data-stu-id="37b58-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="37b58-104">El filtro de representador MIDI representa datos MIDI del filtro de [analizador MIDI](midi-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="37b58-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b58-105">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="37b58-105">Filter Interfaces</span></span>                        | <span data-ttu-id="37b58-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="37b58-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="37b58-107">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="37b58-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="37b58-108">MEDIATYPE \_ MIDI, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="37b58-108">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="37b58-109">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="37b58-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="37b58-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="37b58-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="37b58-111">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="37b58-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="37b58-112">No aplicable</span><span class="sxs-lookup"><span data-stu-id="37b58-112">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="37b58-113">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="37b58-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="37b58-114">No aplicable</span><span class="sxs-lookup"><span data-stu-id="37b58-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="37b58-115">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="37b58-115">Filter CLSID</span></span>                             | <span data-ttu-id="37b58-116">CLSID \_ AVIMIDIRender</span><span class="sxs-lookup"><span data-stu-id="37b58-116">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="37b58-117">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="37b58-117">Property Page CLSID</span></span>                      | <span data-ttu-id="37b58-118">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="37b58-118">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="37b58-119">Executable</span><span class="sxs-lookup"><span data-stu-id="37b58-119">Executable</span></span>                               | <span data-ttu-id="37b58-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="37b58-120">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="37b58-121">Fundament</span><span class="sxs-lookup"><span data-stu-id="37b58-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="37b58-122">MÉRITO \_ preferido</span><span class="sxs-lookup"><span data-stu-id="37b58-122">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="37b58-123">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="37b58-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="37b58-124">CLSID \_ MidiRendererCategory</span><span class="sxs-lookup"><span data-stu-id="37b58-124">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="37b58-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37b58-125">Remarks</span></span>

<span data-ttu-id="37b58-126">El GUID para el tipo de formato es **null**, pero el bloque de formato contiene la siguiente estructura:</span><span class="sxs-lookup"><span data-stu-id="37b58-126">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="37b58-127">El miembro **dwDivision** especifica la división de tiempo del archivo.</span><span class="sxs-lookup"><span data-stu-id="37b58-127">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="37b58-128">La división de tiempo se proporciona en el encabezado de cualquier archivo MIDI estándar (SMF) del `MThd` fragmento.</span><span class="sxs-lookup"><span data-stu-id="37b58-128">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="37b58-129">El representador MIDI establece esta propiedad en el flujo de datos MIDI mediante una llamada a la función **midiStreamProperty** .</span><span class="sxs-lookup"><span data-stu-id="37b58-129">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="37b58-130">Los ejemplos del filtro del analizador MIDI contienen un segundo de datos MIDI.</span><span class="sxs-lookup"><span data-stu-id="37b58-130">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="37b58-131">El representador MIDI utiliza la función **midiStreamOut** para representar los datos MIDI.</span><span class="sxs-lookup"><span data-stu-id="37b58-131">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="37b58-132">Cada ejemplo es un punto de sincronización: el inicio del búfer contiene todos los comandos necesarios para establecer el estado correcto para representar ese búfer.</span><span class="sxs-lookup"><span data-stu-id="37b58-132">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="37b58-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37b58-133">Requirements</span></span>



| <span data-ttu-id="37b58-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="37b58-134">Requirement</span></span> | <span data-ttu-id="37b58-135">Value</span><span class="sxs-lookup"><span data-stu-id="37b58-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b58-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37b58-136">Header</span></span><br/> | <dl> <span data-ttu-id="37b58-137"><dt>Windows. Devices. MIDI. h</dt></span><span class="sxs-lookup"><span data-stu-id="37b58-137"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b58-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="37b58-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b58-139">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="37b58-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




