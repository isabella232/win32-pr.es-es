---
title: Elemento EapType (mspeapuserpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema baseeapuserpropertiesv1. Para mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187838"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a><span data-ttu-id="59ec4-105">Elemento EapType (mspeapuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="59ec4-105">EapType Element (mspeapuserpropertiesv1schema)</span></span>

<span data-ttu-id="59ec4-106">El elemento **EapType** es un tipo derivado del elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) del esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="59ec4-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType
        "
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="59ec4-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="59ec4-107">Child elements</span></span>



| <span data-ttu-id="59ec4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="59ec4-108">Element</span></span>                                                                               | <span data-ttu-id="59ec4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="59ec4-109">Type</span></span>                                                                                      | <span data-ttu-id="59ec4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="59ec4-110">Description</span></span>                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59ec4-111">**Participante**</span><span class="sxs-lookup"><span data-stu-id="59ec4-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | <span data-ttu-id="59ec4-112">El elemento [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) identifica el método interno y las credenciales que se van a utilizar con ese método.</span><span class="sxs-lookup"><span data-stu-id="59ec4-112">The [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) element identifies the inner method and the credentials to be used with that method.</span></span> <span data-ttu-id="59ec4-113">Cuando la configuración de PEAP está configurada para el acceso de invitado de PEAP, este elemento no está presente.</span><span class="sxs-lookup"><span data-stu-id="59ec4-113">When PEAP configuration is configured for PEAP guest access, this element is absent.</span></span><br/>                                  |
| [<span data-ttu-id="59ec4-114">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="59ec4-114">**PeapExtensions**</span></span>](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [<span data-ttu-id="59ec4-115">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="59ec4-115">**PeapExtensionsType**</span></span>](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | <span data-ttu-id="59ec4-116">El elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="59ec4-116">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <br/> <span data-ttu-id="59ec4-117">El elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="59ec4-117">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="59ec4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59ec4-118">Requirements</span></span>



| <span data-ttu-id="59ec4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ec4-119">Requirement</span></span> | <span data-ttu-id="59ec4-120">Value</span><span class="sxs-lookup"><span data-stu-id="59ec4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59ec4-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ec4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="59ec4-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="59ec4-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59ec4-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ec4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="59ec4-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="59ec4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59ec4-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="59ec4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ec4-126">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="59ec4-126">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="59ec4-127">Esquema mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="59ec4-127">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





