---
description: Especifica una clase de servicio de programador de clases multimedia (MMCSS) para los subprocesos de procesamiento de audio en el lector de origen o el escritor de receptores.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: MF_READWRITE_MMCSS_CLASS_AUDIO atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705799"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a><span data-ttu-id="df81a-103">MF \_ ReadWrite \_ \_ Class ( \_ atributo de audio)</span><span class="sxs-lookup"><span data-stu-id="df81a-103">MF\_READWRITE\_MMCSS\_CLASS\_AUDIO attribute</span></span>

<span data-ttu-id="df81a-104">Especifica una clase de [servicio de programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para los subprocesos de procesamiento de audio en el lector de origen o el escritor de receptores.</span><span class="sxs-lookup"><span data-stu-id="df81a-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for audio-processing threads in the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="df81a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="df81a-105">Data type</span></span>

<span data-ttu-id="df81a-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="df81a-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="df81a-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="df81a-107">Get/set</span></span>

<span data-ttu-id="df81a-108">Para obtener este atributo, llame a [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="df81a-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="df81a-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="df81a-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="df81a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df81a-110">Remarks</span></span>

<span data-ttu-id="df81a-111">Opcionalmente, establezca este atributo al crear una instancia del [lector de origen](source-reader.md) o del [escritor de receptores](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="df81a-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="df81a-112">El valor del atributo debe ser un nombre de clase MMCSS válido.</span><span class="sxs-lookup"><span data-stu-id="df81a-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="df81a-113">Si se establece este atributo, el lector de origen o el escritor receptor registra sus subprocesos de procesamiento de audio con la clase MMCSS especificada.</span><span class="sxs-lookup"><span data-stu-id="df81a-113">If this attribute is set, the Source Reader or Sink Writer registers its audio-processing threads with the specified MMCSS class.</span></span> <span data-ttu-id="df81a-114">MMCSS garantiza que el procesamiento de datos en el lector de origen o el escritor de receptores tenga prioridad sobre otras tareas del sistema.</span><span class="sxs-lookup"><span data-stu-id="df81a-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="df81a-115">Para especificar la prioridad base para los subprocesos de audio, establezca el atributo de [ \_ audio MF ReadWrite en \_ \_ prioridad \_ ](mf-readwrite-mmcss-priority-audio.md) .</span><span class="sxs-lookup"><span data-stu-id="df81a-115">To specify the base priority for audio threads, set the [MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO](mf-readwrite-mmcss-priority-audio.md) attribute.</span></span> <span data-ttu-id="df81a-116">Si no se establece ese atributo, la prioridad base para los subprocesos de audio es cero.</span><span class="sxs-lookup"><span data-stu-id="df81a-116">If that attribute is not set, the base priority for audio threads is zero.</span></span>

<span data-ttu-id="df81a-117">Este atributo invalida el atributo de [ \_ \_ \_ clase MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) para los subprocesos de procesamiento de audio.</span><span class="sxs-lookup"><span data-stu-id="df81a-117">This attribute overrides the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute for audio-processing threads.</span></span> <span data-ttu-id="df81a-118">Si no se establece ningún atributo, los subprocesos de audio no se registran con MCSS.</span><span class="sxs-lookup"><span data-stu-id="df81a-118">If neither attribute is set, audio threads are not registered with MCSS.</span></span>

<span data-ttu-id="df81a-119">Para la mayoría de las aplicaciones, el problema de audio es mucho más perceptible para el usuario que el problema de vídeo y, por lo tanto, menos aceptable.</span><span class="sxs-lookup"><span data-stu-id="df81a-119">For most applications, audio glitching is much more noticeable to the user than video glitching, and therefore less acceptable.</span></span> <span data-ttu-id="df81a-120">Por esta razón, una aplicación normalmente debe establecer el \_ audio de la clase MF ReadWrite \_ MMCSS \_ \_ en una clase MMCSS de mayor prioridad que la [ \_ clase MF ReadWrite \_ MMCSS \_ ](mf-readwrite-mmcss-class.md).</span><span class="sxs-lookup"><span data-stu-id="df81a-120">For this reason, an application should typically set MF\_READWRITE\_MMCSS\_CLASS\_AUDIO to a higher-priority MMCSS class than [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md).</span></span> <span data-ttu-id="df81a-121">Esto garantiza que el procesamiento de audio tenga mayor prioridad que otras tareas.</span><span class="sxs-lookup"><span data-stu-id="df81a-121">This ensures that audio processing is given higher priority than other tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="df81a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df81a-122">Requirements</span></span>



| <span data-ttu-id="df81a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="df81a-123">Requirement</span></span> | <span data-ttu-id="df81a-124">Value</span><span class="sxs-lookup"><span data-stu-id="df81a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="df81a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df81a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="df81a-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="df81a-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="df81a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df81a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="df81a-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="df81a-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="df81a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df81a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="df81a-130"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="df81a-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df81a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="df81a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df81a-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="df81a-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
