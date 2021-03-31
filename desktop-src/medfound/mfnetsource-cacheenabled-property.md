---
description: Especifica si el origen de red almacena en caché el contenido.
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: Propiedad MFNETSOURCE_CACHEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6f38398e44eaa25da7a5b1f88a76edb8e40924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908247"
---
# <a name="mfnetsource_cacheenabled-property"></a><span data-ttu-id="5c808-103">\_Propiedad CACHEENABLED de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="5c808-103">MFNETSOURCE\_CACHEENABLED property</span></span>

<span data-ttu-id="5c808-104">Especifica si el origen de red almacena en caché el contenido.</span><span class="sxs-lookup"><span data-stu-id="5c808-104">Specifies whether the network source caches content.</span></span>



<span data-ttu-id="5c808-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5c808-105">Data type</span></span>

<span data-ttu-id="5c808-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="5c808-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5c808-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="5c808-107">PROPVARIANT member</span></span>

<span data-ttu-id="5c808-108">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="5c808-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="5c808-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5c808-109">VT\_I4</span></span>

<span data-ttu-id="5c808-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="5c808-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5c808-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c808-111">Remarks</span></span>

<span data-ttu-id="5c808-112">La constante **MFNETSOURCE \_ CACHEENABLED** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5c808-112">The constant **MFNETSOURCE\_CACHEENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="5c808-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="5c808-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="5c808-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="5c808-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="5c808-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="5c808-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="5c808-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5c808-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="5c808-117">El valor predeterminado de esta propiedad es **true**.</span><span class="sxs-lookup"><span data-stu-id="5c808-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c808-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c808-118">Requirements</span></span>



| <span data-ttu-id="5c808-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c808-119">Requirement</span></span> | <span data-ttu-id="5c808-120">Value</span><span class="sxs-lookup"><span data-stu-id="5c808-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c808-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c808-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c808-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5c808-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5c808-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c808-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c808-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c808-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5c808-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c808-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c808-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c808-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c808-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c808-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c808-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c808-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5c808-129">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c808-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




