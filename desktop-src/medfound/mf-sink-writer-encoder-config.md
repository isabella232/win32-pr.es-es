---
description: Contiene un puntero a un almacén de propiedades con propiedades de codificación.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: MF_SINK_WRITER_ENCODER_CONFIG atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814891"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a><span data-ttu-id="889e1-103">\_Atributo de \_ \_ configuración del codificador del escritor de receptor MF \_</span><span class="sxs-lookup"><span data-stu-id="889e1-103">MF\_SINK\_WRITER\_ENCODER\_CONFIG attribute</span></span>

<span data-ttu-id="889e1-104">Contiene un puntero a un almacén de propiedades con propiedades de codificación.</span><span class="sxs-lookup"><span data-stu-id="889e1-104">Contains a pointer to a property store with encoding properties.</span></span>

## <a name="data-type"></a><span data-ttu-id="889e1-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="889e1-105">Data type</span></span>

<span data-ttu-id="889e1-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="889e1-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="889e1-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="889e1-107">Remarks</span></span>

<span data-ttu-id="889e1-108">El valor de este atributo es [_ *IPropertyStore* \*](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="889e1-108">The value of this attribute is an [_ *IPropertyStore*\*](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer.</span></span>

<span data-ttu-id="889e1-109">Este atributo permite que una aplicación establezca las propiedades de codificación al utilizar el [escritor del receptor](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="889e1-109">This attribute enables an application to set encoding properties when using the [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="889e1-110">Para establecer este atributo, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="889e1-110">To set this attribute, perform the following steps:</span></span>

1.  <span data-ttu-id="889e1-111">Llame a [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para crear un nuevo almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="889e1-111">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a new property store.</span></span>
2.  <span data-ttu-id="889e1-112">Establezca las propiedades del codificador en el almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="889e1-112">Set encoder properties on the property store.</span></span> <span data-ttu-id="889e1-113">Las propiedades disponibles dependen del codificador.</span><span class="sxs-lookup"><span data-stu-id="889e1-113">The available properties depends on the encoder.</span></span> <span data-ttu-id="889e1-114">Para obtener más información, consulte [objetos codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="889e1-114">For more information, see [Codec Objects](codecobjects.md).</span></span>
3.  <span data-ttu-id="889e1-115">Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="889e1-115">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
4.  <span data-ttu-id="889e1-116">Llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) para establecer el puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) en el almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="889e1-116">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer on the attribute store.</span></span>
5.  <span data-ttu-id="889e1-117">Cree una nueva instancia del escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="889e1-117">Create a new instance of the Sink Writer.</span></span> <span data-ttu-id="889e1-118">Pase el puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) a la función de creación.</span><span class="sxs-lookup"><span data-stu-id="889e1-118">Pass the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer to the creation function.</span></span> <span data-ttu-id="889e1-119">Para obtener más información, vea [atributos del escritor de receptor](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="889e1-119">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

<span data-ttu-id="889e1-120">El escritor del receptor establece las propiedades en el codificador antes de establecer los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="889e1-120">The Sink Writer sets the properties on the encoder before setting the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="889e1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="889e1-121">Requirements</span></span>



| <span data-ttu-id="889e1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="889e1-122">Requirement</span></span> | <span data-ttu-id="889e1-123">Value</span><span class="sxs-lookup"><span data-stu-id="889e1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="889e1-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="889e1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="889e1-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="889e1-125">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="889e1-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="889e1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="889e1-127">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="889e1-127">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="889e1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="889e1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="889e1-129"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="889e1-129"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="889e1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="889e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="889e1-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="889e1-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="889e1-132">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="889e1-132">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="889e1-133">Atributos del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="889e1-133">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 
