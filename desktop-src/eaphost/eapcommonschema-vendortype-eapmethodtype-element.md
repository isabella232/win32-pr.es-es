---
title: VendorType (EapMethodType), elemento
description: Obtenga información sobre el elemento VendorType (EapMethodType). Este elemento es el tipo definido por el proveedor para el método.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Elemento VendorType de VendorType
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488271"
---
# <a name="vendortype-eapmethodtype-element"></a><span data-ttu-id="9bb48-105">VendorType (EapMethodType), elemento</span><span class="sxs-lookup"><span data-stu-id="9bb48-105">VendorType (EapMethodType) Element</span></span>

<span data-ttu-id="9bb48-106">El elemento **VendorType (EapMethodType)** es el tipo definido por el proveedor para el método.</span><span class="sxs-lookup"><span data-stu-id="9bb48-106">The **VendorType (EapMethodType)** element is the vendor defined type for the method.</span></span>

<span data-ttu-id="9bb48-107">El elemento **VendorType** es opcional.</span><span class="sxs-lookup"><span data-stu-id="9bb48-107">The **VendorType** element is optional.</span></span> <span data-ttu-id="9bb48-108">Si se utiliza, **VendorType** es un número único emitido por Internet Assigned Numbers Authority (IANA).</span><span class="sxs-lookup"><span data-stu-id="9bb48-108">If used, the **VendorType** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

<span data-ttu-id="9bb48-109">El elemento **VendorType** se define mediante el tipo complejo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb48-109">The **VendorType** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bb48-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bb48-110">Requirements</span></span>



| <span data-ttu-id="9bb48-111">Role</span><span class="sxs-lookup"><span data-stu-id="9bb48-111">Role</span></span> | <span data-ttu-id="9bb48-112">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9bb48-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="9bb48-113">Remoto</span><span class="sxs-lookup"><span data-stu-id="9bb48-113">Client</span></span><br/> | <span data-ttu-id="9bb48-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9bb48-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9bb48-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="9bb48-115">Server</span></span><br/> | <span data-ttu-id="9bb48-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9bb48-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9bb48-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bb48-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="9bb48-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="9bb48-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9bb48-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="9bb48-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="9bb48-120">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="9bb48-120">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="9bb48-121">Esquema eapcommon</span><span class="sxs-lookup"><span data-stu-id="9bb48-121">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





