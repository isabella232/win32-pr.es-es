---
description: Establece la prioridad base para los subprocesos de procesamiento de audio creados por el lector de origen o el escritor del receptor.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: MF_READWRITE_MMCSS_PRIORITY_AUDIO atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705798"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a><span data-ttu-id="0cca5-103">MF \_ ReadWrite \_ / \_ atributo de audio prioritario de MMCSS \_</span><span class="sxs-lookup"><span data-stu-id="0cca5-103">MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO attribute</span></span>

<span data-ttu-id="0cca5-104">Establece la prioridad base para los subprocesos de procesamiento de audio creados por el lector de origen o el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="0cca5-104">Sets the base priority for audio-processing threads created by the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="0cca5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0cca5-105">Data type</span></span>

<span data-ttu-id="0cca5-106">**INT32** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="0cca5-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0cca5-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="0cca5-107">Get/set</span></span>

<span data-ttu-id="0cca5-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0cca5-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0cca5-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0cca5-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0cca5-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cca5-110">Remarks</span></span>

<span data-ttu-id="0cca5-111">Opcionalmente, establezca este atributo al crear una instancia del [lector de origen](source-reader.md) o del [escritor de receptores](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="0cca5-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="0cca5-112">Si establece este atributo, establezca también el atributo de audio de la [ \_ \_ \_ \_ clase MF ReadWrite MMCSS](mf-readwrite-mmcss-class-audio.md) .</span><span class="sxs-lookup"><span data-stu-id="0cca5-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute.</span></span> <span data-ttu-id="0cca5-113">De lo contrario, se omite este atributo.</span><span class="sxs-lookup"><span data-stu-id="0cca5-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="0cca5-114">Cuando el lector de origen o el escritor receptor registra los subprocesos de procesamiento de audio con el [servicio Programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md), el valor de este atributo especifica la prioridad de subproceso base.</span><span class="sxs-lookup"><span data-stu-id="0cca5-114">When the Source Reader or Sink Writer registers audio-processing threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="0cca5-115">Si no se establece este atributo, el valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="0cca5-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cca5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cca5-116">Requirements</span></span>



| <span data-ttu-id="0cca5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cca5-117">Requirement</span></span> | <span data-ttu-id="0cca5-118">Value</span><span class="sxs-lookup"><span data-stu-id="0cca5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cca5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cca5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0cca5-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="0cca5-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0cca5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cca5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0cca5-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="0cca5-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0cca5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cca5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cca5-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cca5-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cca5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cca5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cca5-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0cca5-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
