---
description: Duración del streaming acelerado para el origen de red, en milisegundos.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: Propiedad MFNETSOURCE_ACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908249"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a><span data-ttu-id="e7d8c-103">\_Propiedad ACCELERATEDSTREAMINGDURATION de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="e7d8c-103">MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="e7d8c-104">Duración del streaming acelerado para el origen de red, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="e7d8c-104">Duration of accelerated streaming for the network source, in milliseconds.</span></span>



<span data-ttu-id="e7d8c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e7d8c-105">Data type</span></span>

<span data-ttu-id="e7d8c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e7d8c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e7d8c-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e7d8c-107">PROPVARIANT member</span></span>

<span data-ttu-id="e7d8c-108">**DWORD** (almacenado como **Long**)</span><span class="sxs-lookup"><span data-stu-id="e7d8c-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="e7d8c-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e7d8c-109">VT\_I4</span></span>

<span data-ttu-id="e7d8c-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="e7d8c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e7d8c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7d8c-111">Remarks</span></span>

<span data-ttu-id="e7d8c-112">La constante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e7d8c-112">The constant **MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="e7d8c-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="e7d8c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e7d8c-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="e7d8c-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="e7d8c-115">Para establecer la propiedad, pase un objeto **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="e7d8c-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="e7d8c-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e7d8c-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="e7d8c-117">Esta propiedad se aplica a la característica de inicio rápido de Windows Media Services, que reproduce el contenido rápidamente sin tener que esperar al almacenamiento en búfer inicial largo.</span><span class="sxs-lookup"><span data-stu-id="e7d8c-117">This property applies to the Fast Start feature of Windows Media Services, which plays content quickly without waiting for lengthy initial buffering.</span></span> <span data-ttu-id="e7d8c-118">Al usar Inicio rápido, el servidor que ejecuta Windows Media Services enviará algunos datos al principio del contenido con una velocidad mayor que la especificada en la velocidad de bits del contenido.</span><span class="sxs-lookup"><span data-stu-id="e7d8c-118">When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.</span></span>

<span data-ttu-id="e7d8c-119">El valor predeterminado de esta propiedad es 10.000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="e7d8c-119">The default value of this property is 10,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d8c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7d8c-120">Requirements</span></span>



| <span data-ttu-id="e7d8c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7d8c-121">Requirement</span></span> | <span data-ttu-id="e7d8c-122">Value</span><span class="sxs-lookup"><span data-stu-id="e7d8c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d8c-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7d8c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d8c-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e7d8c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e7d8c-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7d8c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d8c-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7d8c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e7d8c-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7d8c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7d8c-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7d8c-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7d8c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7d8c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d8c-130">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7d8c-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e7d8c-131">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="e7d8c-131">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="e7d8c-132">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7d8c-132">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




