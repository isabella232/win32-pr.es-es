---
description: Establece la prioridad de subproceso base para el lector de origen o el escritor del receptor.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: MF_READWRITE_MMCSS_PRIORITY atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083329"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a><span data-ttu-id="b4b43-103">MF \_ ReadWrite \_ , \_ atributo Priority</span><span class="sxs-lookup"><span data-stu-id="b4b43-103">MF\_READWRITE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="b4b43-104">Establece la prioridad de subproceso base para el lector de origen o el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="b4b43-104">Sets the base thread priority for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b4b43-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b4b43-105">Data type</span></span>

<span data-ttu-id="b4b43-106">**INT32** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="b4b43-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b4b43-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="b4b43-107">Get/set</span></span>

<span data-ttu-id="b4b43-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b4b43-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b4b43-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b4b43-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b43-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4b43-110">Remarks</span></span>

<span data-ttu-id="b4b43-111">Opcionalmente, establezca este atributo al crear una instancia del [lector de origen](source-reader.md) o del [escritor de receptores](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="b4b43-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="b4b43-112">Si establece este atributo, establezca también el atributo [de \_ \_ \_ clase MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) .</span><span class="sxs-lookup"><span data-stu-id="b4b43-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute.</span></span> <span data-ttu-id="b4b43-113">De lo contrario, se omite este atributo.</span><span class="sxs-lookup"><span data-stu-id="b4b43-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="b4b43-114">Cuando el lector de origen o el escritor receptor registra los subprocesos con el [servicio Programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md), el valor de este atributo especifica la prioridad de subproceso base.</span><span class="sxs-lookup"><span data-stu-id="b4b43-114">When the Source Reader or Sink Writer registers threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="b4b43-115">Si no se establece este atributo, el valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="b4b43-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b43-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4b43-116">Requirements</span></span>



| <span data-ttu-id="b4b43-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4b43-117">Requirement</span></span> | <span data-ttu-id="b4b43-118">Value</span><span class="sxs-lookup"><span data-stu-id="b4b43-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b43-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4b43-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b43-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="b4b43-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b4b43-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4b43-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b43-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="b4b43-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b4b43-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4b43-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b43-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b43-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b43-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4b43-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b43-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4b43-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
