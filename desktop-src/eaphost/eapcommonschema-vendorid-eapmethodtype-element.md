---
title: VendorId (EapMethodType), elemento
description: Hace referencia al proveedor que definió el método si el elemento Type (EapMethodType) es 254 (un método EAP expandido).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Elemento VendorId EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534276"
---
# <a name="vendorid-eapmethodtype-element"></a><span data-ttu-id="2abbf-104">VendorId (EapMethodType), elemento</span><span class="sxs-lookup"><span data-stu-id="2abbf-104">VendorId (EapMethodType) Element</span></span>

<span data-ttu-id="2abbf-105">El elemento **VendorId (EapMethodType)** hace referencia al proveedor que definió el método si el elemento [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) es 254 (un método EAP expandido).</span><span class="sxs-lookup"><span data-stu-id="2abbf-105">The **VendorId (EapMethodType)** element refers to the vendor who defined the method if the [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span>

<span data-ttu-id="2abbf-106">**VendorId** es opcional.</span><span class="sxs-lookup"><span data-stu-id="2abbf-106">The **VendorId** is optional.</span></span> <span data-ttu-id="2abbf-107">Si se usa, el **VendorId** es un número único emitido por Internet Assigned Numbers Authority (IANA).</span><span class="sxs-lookup"><span data-stu-id="2abbf-107">If used, the **VendorId** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="2abbf-108">El elemento **VendorId** se define mediante el tipo complejo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2abbf-108">The **VendorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2abbf-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2abbf-109">Remarks</span></span>

<span data-ttu-id="2abbf-110">No es necesario que los elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) y **VendorId** sean los mismos para un método determinado.</span><span class="sxs-lookup"><span data-stu-id="2abbf-110">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and **VendorId** elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2abbf-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2abbf-111">Requirements</span></span>



| <span data-ttu-id="2abbf-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2abbf-112">Requirement</span></span> | <span data-ttu-id="2abbf-113">Value</span><span class="sxs-lookup"><span data-stu-id="2abbf-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2abbf-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2abbf-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2abbf-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2abbf-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2abbf-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2abbf-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2abbf-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2abbf-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2abbf-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2abbf-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="2abbf-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="2abbf-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2abbf-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="2abbf-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="2abbf-121">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="2abbf-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2abbf-122">Esquema eapcommon</span><span class="sxs-lookup"><span data-stu-id="2abbf-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





