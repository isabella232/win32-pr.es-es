---
description: Establece la configuración de flujo para el origen de medios WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: Propiedad MFPKEY_SBESourceMode (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001626"
---
# <a name="mfpkey_sbesourcemode-property"></a><span data-ttu-id="c30c1-103">\_Propiedad SBESourceMode de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="c30c1-103">MFPKEY\_SBESourceMode property</span></span>

<span data-ttu-id="c30c1-104">Establece la configuración de flujo para el origen de medios WTV.</span><span class="sxs-lookup"><span data-stu-id="c30c1-104">Sets the stream configuration for the WTV media source.</span></span>



<span data-ttu-id="c30c1-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c30c1-105">Data type</span></span>

<span data-ttu-id="c30c1-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="c30c1-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c30c1-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="c30c1-107">PROPVARIANT member</span></span>

<span data-ttu-id="c30c1-108">**INT**</span><span class="sxs-lookup"><span data-stu-id="c30c1-108">**INT**</span></span>

<span data-ttu-id="c30c1-109">VT \_ int</span><span class="sxs-lookup"><span data-stu-id="c30c1-109">VT\_INT</span></span>

<span data-ttu-id="c30c1-110">**intVal**</span><span class="sxs-lookup"><span data-stu-id="c30c1-110">**intVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c30c1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c30c1-111">Remarks</span></span>

<span data-ttu-id="c30c1-112">Utilice esta propiedad para configurar el origen de medios WTV.</span><span class="sxs-lookup"><span data-stu-id="c30c1-112">Use this property to configure the WTV media source.</span></span> <span data-ttu-id="c30c1-113">Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="c30c1-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="c30c1-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="c30c1-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="c30c1-115">El origen de medios WTV lee archivos de programas de TV grabados de Windows (. WTV y. ms-drv).</span><span class="sxs-lookup"><span data-stu-id="c30c1-115">The WTV media source reads Windows Recorded TV Show (.wtv and .ms-drv) files.</span></span>

<span data-ttu-id="c30c1-116">Esta propiedad debe tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c30c1-116">This property must have one of the following values.</span></span>

-   <span data-ttu-id="c30c1-117">1: asigne secuencias de audio disponibles a una sola salida, según el sistema local.</span><span class="sxs-lookup"><span data-stu-id="c30c1-117">1: Map available audio streams to a single output, based on the system local.</span></span> <span data-ttu-id="c30c1-118">Este modo es adecuado para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="c30c1-118">This mode is appropriate for playback.</span></span> <span data-ttu-id="c30c1-119">(Valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="c30c1-119">(Default.)</span></span>
-   2. <span data-ttu-id="c30c1-120">Se seleccionan todas las secuencias de audio y subsecuencias (como el título y los flujos de datos).</span><span class="sxs-lookup"><span data-stu-id="c30c1-120">All audio streams and substreams (such as caption and data streams) are selected.</span></span> <span data-ttu-id="c30c1-121">Este modo es adecuado para remuxing o la transcodificación.</span><span class="sxs-lookup"><span data-stu-id="c30c1-121">This mode is appropriate for remuxing or transcoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="c30c1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c30c1-122">Requirements</span></span>



| <span data-ttu-id="c30c1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c30c1-123">Requirement</span></span> | <span data-ttu-id="c30c1-124">Value</span><span class="sxs-lookup"><span data-stu-id="c30c1-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c30c1-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c30c1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c30c1-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="c30c1-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c30c1-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c30c1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c30c1-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="c30c1-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c30c1-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c30c1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c30c1-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c30c1-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c30c1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c30c1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c30c1-132">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c30c1-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
