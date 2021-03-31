---
title: AuthorId (EapMethodType), elemento
description: Obtenga información sobre el elemento AuthorId (EapMethodType). El elemento AuthorID (EapMethodType) hace referencia al autor del método.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Elemento AuthorId EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995638"
---
# <a name="authorid-eapmethodtype-element"></a><span data-ttu-id="a1ecf-105">AuthorId (EapMethodType), elemento</span><span class="sxs-lookup"><span data-stu-id="a1ecf-105">AuthorId (EapMethodType) Element</span></span>

<span data-ttu-id="a1ecf-106">El elemento **AuthorId (EapMethodType)** hace referencia al autor del método.</span><span class="sxs-lookup"><span data-stu-id="a1ecf-106">The **AuthorId (EapMethodType)** element refers to the method author.</span></span>

<span data-ttu-id="a1ecf-107">AuthorId es un número único emitido por Internet Assigned Numbers Authority (IANA).</span><span class="sxs-lookup"><span data-stu-id="a1ecf-107">The AuthorId is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="a1ecf-108">El elemento **AuthorId** se define mediante el tipo complejo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a1ecf-108">The **AuthorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ecf-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1ecf-109">Remarks</span></span>

<span data-ttu-id="a1ecf-110">No es necesario que los elementos **AuthorId** y [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) sean los mismos para un método determinado.</span><span class="sxs-lookup"><span data-stu-id="a1ecf-110">The **AuthorId** and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1ecf-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1ecf-111">Requirements</span></span>



| <span data-ttu-id="a1ecf-112">Role</span><span class="sxs-lookup"><span data-stu-id="a1ecf-112">Role</span></span> | <span data-ttu-id="a1ecf-113">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a1ecf-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="a1ecf-114">Remoto</span><span class="sxs-lookup"><span data-stu-id="a1ecf-114">Client</span></span><br/> | <span data-ttu-id="a1ecf-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a1ecf-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1ecf-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="a1ecf-116">Server</span></span><br/> | <span data-ttu-id="a1ecf-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1ecf-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1ecf-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1ecf-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1ecf-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="a1ecf-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a1ecf-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="a1ecf-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="a1ecf-121">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="a1ecf-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a1ecf-122">Esquema eapcommon</span><span class="sxs-lookup"><span data-stu-id="a1ecf-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





