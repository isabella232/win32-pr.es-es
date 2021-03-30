---
description: Especifica una clase de servicio del programador de clases multimedia (MMCSS) para el lector de origen o el escritor del receptor.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: MF_READWRITE_MMCSS_CLASS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817126"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a><span data-ttu-id="7c8f8-103">MF \_ ReadWrite \_ ( \_ atributo de clase)</span><span class="sxs-lookup"><span data-stu-id="7c8f8-103">MF\_READWRITE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="7c8f8-104">Especifica una clase de [servicio del programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para el lector de origen o el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="7c8f8-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c8f8-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7c8f8-105">Data type</span></span>

<span data-ttu-id="7c8f8-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7c8f8-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="7c8f8-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="7c8f8-107">Get/set</span></span>

<span data-ttu-id="7c8f8-108">Para obtener este atributo, llame a [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="7c8f8-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="7c8f8-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="7c8f8-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c8f8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c8f8-110">Remarks</span></span>

<span data-ttu-id="7c8f8-111">Opcionalmente, establezca este atributo al crear una instancia del [lector de origen](source-reader.md) o del [escritor de receptores](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="7c8f8-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="7c8f8-112">El valor del atributo debe ser un nombre de clase MMCSS válido.</span><span class="sxs-lookup"><span data-stu-id="7c8f8-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="7c8f8-113">Si se establece este atributo, el lector de origen o el escritor receptor registra todos los subprocesos con la clase MMCSS especificada.</span><span class="sxs-lookup"><span data-stu-id="7c8f8-113">If this attribute is set, the Source Reader or Sink Writer registers all of its threads with the specified MMCSS class.</span></span> <span data-ttu-id="7c8f8-114">MMCSS garantiza que el procesamiento de datos en el lector de origen o el escritor de receptores tenga prioridad sobre otras tareas del sistema.</span><span class="sxs-lookup"><span data-stu-id="7c8f8-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="7c8f8-115">Para especificar la prioridad base, establezca el atributo de [ \_ \_ \_ prioridad MF ReadWrite MMCSS](mf-readwrite-mmcss-priority.md) .</span><span class="sxs-lookup"><span data-stu-id="7c8f8-115">To specify the base priority, set the [MF\_READWRITE\_MMCSS\_PRIORITY](mf-readwrite-mmcss-priority.md) attribute.</span></span> <span data-ttu-id="7c8f8-116">Si no se establece ese atributo, la prioridad base es cero.</span><span class="sxs-lookup"><span data-stu-id="7c8f8-116">If that attribute is not set, the base priority is zero.</span></span>

<span data-ttu-id="7c8f8-117">En el caso de los subprocesos de procesamiento de audio, el atributo de audio de la [ \_ \_ \_ \_ clase MF ReadWrite MMCSS](mf-readwrite-mmcss-class-audio.md) (si se establece) invalida este atributo.</span><span class="sxs-lookup"><span data-stu-id="7c8f8-117">For audio-processing threads, the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute (if set) overrides this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c8f8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c8f8-118">Requirements</span></span>



| <span data-ttu-id="7c8f8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c8f8-119">Requirement</span></span> | <span data-ttu-id="7c8f8-120">Value</span><span class="sxs-lookup"><span data-stu-id="7c8f8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c8f8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c8f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7c8f8-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="7c8f8-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7c8f8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c8f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7c8f8-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="7c8f8-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7c8f8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c8f8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c8f8-126"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c8f8-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c8f8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c8f8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c8f8-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c8f8-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
