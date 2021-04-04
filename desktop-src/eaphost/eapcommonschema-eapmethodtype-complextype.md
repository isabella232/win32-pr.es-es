---
title: Tipo complejo de EapMethodType
description: Define los elementos que identifican de forma única un solo tipo de método EAP, VendorId, VendorType y AuthorId.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- Tipo complejo EapMethodType EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802533"
---
# <a name="eapmethodtype-complex-type"></a><span data-ttu-id="c08b6-104">Tipo complejo de EapMethodType</span><span class="sxs-lookup"><span data-stu-id="c08b6-104">EapMethodType Complex Type</span></span>

<span data-ttu-id="c08b6-105">El tipo complejo **EapMethodType** define los elementos que identifican de forma única un solo método EAP: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)y [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).</span><span class="sxs-lookup"><span data-stu-id="c08b6-105">The **EapMethodType** complex type defines the elements that uniquely identify a single EAP method: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md), and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).</span></span>

<span data-ttu-id="c08b6-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) y [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) son elementos obligatorios, mientras que [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) y [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) solo son necesarios cuando el elemento **Type** es 254 (un método EAP ampliado).</span><span class="sxs-lookup"><span data-stu-id="c08b6-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) are mandatory elements, whereas [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) are required only when the **Type** element is 254 (an expanded EAP method).</span></span>

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c08b6-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c08b6-107">Child elements</span></span>



| <span data-ttu-id="c08b6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c08b6-108">Element</span></span>                                                                | <span data-ttu-id="c08b6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c08b6-109">Type</span></span>         | <span data-ttu-id="c08b6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c08b6-110">Description</span></span>                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c08b6-111">**AuthorId**</span><span class="sxs-lookup"><span data-stu-id="c08b6-111">**AuthorId**</span></span>](eapcommonschema-authorid-eapmethodtype-element.md)     | <span data-ttu-id="c08b6-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c08b6-112">unsignedInt</span></span>  | <span data-ttu-id="c08b6-113">Hace referencia al autor del método.</span><span class="sxs-lookup"><span data-stu-id="c08b6-113">Refers to the method author.</span></span> <br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="c08b6-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c08b6-114">**Type**</span></span>](eapcommonschema-type-eapmethodtype-element.md)             | <span data-ttu-id="c08b6-115">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="c08b6-115">unsignedByte</span></span> | <span data-ttu-id="c08b6-116">Hace referencia al tipo de método EAP.</span><span class="sxs-lookup"><span data-stu-id="c08b6-116">Refers to the EAP method type.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="c08b6-117">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="c08b6-117">**VendorId**</span></span>](eapcommonschema-vendorid-eapmethodtype-element.md)     | <span data-ttu-id="c08b6-118">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c08b6-118">unsignedInt</span></span>  | <span data-ttu-id="c08b6-119">Hace referencia al proveedor que definió el método, si el elemento [**Type**](eapcommonschema-type-eapmethodtype-element.md) es 254 (un método EAP expandido).</span><span class="sxs-lookup"><span data-stu-id="c08b6-119">Refers to the vendor who defined the method - if the [**Type**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span> <span data-ttu-id="c08b6-120">[**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="c08b6-120">The [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) is optional.</span></span> <br/> |
| [<span data-ttu-id="c08b6-121">**VendorType**</span><span class="sxs-lookup"><span data-stu-id="c08b6-121">**VendorType**</span></span>](eapcommonschema-vendortype-eapmethodtype-element.md) | <span data-ttu-id="c08b6-122">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c08b6-122">unsignedInt</span></span>  | <span data-ttu-id="c08b6-123">Es el tipo definido por el proveedor para el método.</span><span class="sxs-lookup"><span data-stu-id="c08b6-123">Is the vendor defined type for the method.</span></span> <span data-ttu-id="c08b6-124">[**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="c08b6-124">The [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) is optional.</span></span> <br/>                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="c08b6-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c08b6-125">Remarks</span></span>

<span data-ttu-id="c08b6-126">No es necesario que los elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) y [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) sean los mismos para un método determinado.</span><span class="sxs-lookup"><span data-stu-id="c08b6-126">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

<span data-ttu-id="c08b6-127">Los elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) y [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) son un número único emitido por Internet Assigned Numbers Authority (IANA).</span><span class="sxs-lookup"><span data-stu-id="c08b6-127">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) and [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) elements are each a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

## <a name="requirements"></a><span data-ttu-id="c08b6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c08b6-128">Requirements</span></span>



| <span data-ttu-id="c08b6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c08b6-129">Requirement</span></span> | <span data-ttu-id="c08b6-130">Value</span><span class="sxs-lookup"><span data-stu-id="c08b6-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c08b6-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c08b6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c08b6-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c08b6-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c08b6-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c08b6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c08b6-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c08b6-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c08b6-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c08b6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c08b6-136">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="c08b6-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c08b6-137">Esquema eapcommon</span><span class="sxs-lookup"><span data-stu-id="c08b6-137">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





