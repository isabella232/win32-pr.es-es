---
title: Tipo complejo de PeapExtensionsType
description: Contiene mejoras de esquema realizadas en Windows 7. Las mejoras futuras del esquema se controlarán mediante PeapExtensionsTypeV2.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- Tipo complejo PeapExtensionsType EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803283"
---
# <a name="peapextensionstype-complex-type"></a><span data-ttu-id="93028-105">Tipo complejo de PeapExtensionsType</span><span class="sxs-lookup"><span data-stu-id="93028-105">PeapExtensionsType Complex Type</span></span>

<span data-ttu-id="93028-106">El tipo complejo **PeapExtensionsType** contiene mejoras de esquema realizadas en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="93028-106">The **PeapExtensionsType** complex type contains schema enhancements made in Windows 7.</span></span> <span data-ttu-id="93028-107">Las mejoras futuras del esquema se controlarán mediante [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span><span class="sxs-lookup"><span data-stu-id="93028-107">Future schema enhancements will be handled by [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="93028-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="93028-108">Child elements</span></span>



| <span data-ttu-id="93028-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="93028-109">Element</span></span>                                                                                                                               | <span data-ttu-id="93028-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="93028-110">Type</span></span> | <span data-ttu-id="93028-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="93028-111">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93028-112">**extendedPeap:PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="93028-112">**extendedPeap:PerformServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | <span data-ttu-id="93028-113">Windows 7 y versiones posteriores: indica si se realiza la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="93028-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                          |
| [<span data-ttu-id="93028-114">**extendedPeap:AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="93028-114">**extendedPeap:AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | <span data-ttu-id="93028-115">Windows 7 y versiones posteriores: indica si se lee el nombre de un servidor.</span><span class="sxs-lookup"><span data-stu-id="93028-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                            |
| [<span data-ttu-id="93028-116">**extendedPeap:IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="93028-116">**extendedPeap:IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | <span data-ttu-id="93028-117">Windows 7 y versiones posteriores: indica si se envía una identidad verdadera o anónima de un usuario.</span><span class="sxs-lookup"><span data-stu-id="93028-117">Windows 7 and later: indicates whether a user's true identity or an anonymous identity is sent.</span></span><br/> |
| [<span data-ttu-id="93028-118">**extendedPeap:PeapExtensionsV2**</span><span class="sxs-lookup"><span data-stu-id="93028-118">**extendedPeap:PeapExtensionsV2**</span></span>](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | <span data-ttu-id="93028-119">Windows 7 y versiones posteriores: permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="93028-119">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                 |



## <a name="remarks"></a><span data-ttu-id="93028-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93028-120">Remarks</span></span>

<span data-ttu-id="93028-121">El elemento **PeapExtensionsType** es opcional.</span><span class="sxs-lookup"><span data-stu-id="93028-121">The **PeapExtensionsType** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="93028-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93028-122">Requirements</span></span>



| <span data-ttu-id="93028-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="93028-123">Requirement</span></span> | <span data-ttu-id="93028-124">Value</span><span class="sxs-lookup"><span data-stu-id="93028-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="93028-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93028-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93028-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="93028-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="93028-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93028-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93028-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="93028-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93028-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="93028-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93028-130">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="93028-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="93028-131">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="93028-131">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="93028-132">Tipos complejos de esquema de mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="93028-132">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





