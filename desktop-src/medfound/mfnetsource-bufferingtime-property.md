---
description: Número de segundos de datos que el origen de red almacena en el búfer en el inicio.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: Propiedad MFNETSOURCE_BUFFERINGTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21c165e58ebd5f2aec0f1ca7ce38281f8c94896d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154965"
---
# <a name="mfnetsource_bufferingtime-property"></a><span data-ttu-id="1836c-103">\_Propiedad BUFFERINGTIME de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="1836c-103">MFNETSOURCE\_BUFFERINGTIME property</span></span>

<span data-ttu-id="1836c-104">Número de segundos de datos que el origen de red almacena en el búfer en el inicio.</span><span class="sxs-lookup"><span data-stu-id="1836c-104">Number of seconds of data that the network source buffers at startup.</span></span>



<span data-ttu-id="1836c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1836c-105">Data type</span></span>

<span data-ttu-id="1836c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="1836c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1836c-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="1836c-107">PROPVARIANT member</span></span>

<span data-ttu-id="1836c-108">**DWORD** (almacenado como **Long**)</span><span class="sxs-lookup"><span data-stu-id="1836c-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="1836c-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1836c-109">VT\_I4</span></span>

<span data-ttu-id="1836c-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="1836c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1836c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1836c-111">Remarks</span></span>

<span data-ttu-id="1836c-112">La constante **MFNETSOURCE \_ BUFFERINGTIME** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1836c-112">The constant **MFNETSOURCE\_BUFFERINGTIME** defines the GUID for this property key.</span></span> <span data-ttu-id="1836c-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="1836c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="1836c-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="1836c-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="1836c-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="1836c-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="1836c-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="1836c-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="1836c-117">El valor predeterminado de esta propiedad es de 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="1836c-117">The default value of this property is 5 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="1836c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1836c-118">Requirements</span></span>



| <span data-ttu-id="1836c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1836c-119">Requirement</span></span> | <span data-ttu-id="1836c-120">Value</span><span class="sxs-lookup"><span data-stu-id="1836c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1836c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1836c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1836c-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1836c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1836c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1836c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1836c-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1836c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1836c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1836c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1836c-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1836c-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1836c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1836c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1836c-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1836c-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1836c-129">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="1836c-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="1836c-130">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1836c-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




