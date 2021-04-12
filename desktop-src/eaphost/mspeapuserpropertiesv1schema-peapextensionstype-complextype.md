---
title: Tipo complejo de PeapExtensionsType (propiedades de conexión)
description: Obtenga información sobre el tipo complejo de PeapExtensionsType. Este tipo permite futuras mejoras en el esquema.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
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
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359424"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a><span data-ttu-id="11748-105">Tipo complejo de PeapExtensionsType (propiedades de conexión)</span><span class="sxs-lookup"><span data-stu-id="11748-105">PeapExtensionsType complex type (connection properties)</span></span>

<span data-ttu-id="11748-106">El tipo complejo **PeapExtensionsType** permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="11748-106">The **PeapExtensionsType** complex type enables future enhancements to the schema.</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="11748-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11748-107">Remarks</span></span>

<span data-ttu-id="11748-108">El tipo complejo **PeapExtensionsType** es opcional.</span><span class="sxs-lookup"><span data-stu-id="11748-108">The **PeapExtensionsType** complex type is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="11748-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11748-109">Requirements</span></span>



| <span data-ttu-id="11748-110">Role</span><span class="sxs-lookup"><span data-stu-id="11748-110">Role</span></span> | <span data-ttu-id="11748-111">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="11748-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="11748-112">Remoto</span><span class="sxs-lookup"><span data-stu-id="11748-112">Client</span></span><br/> | <span data-ttu-id="11748-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="11748-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="11748-114">Servidor</span><span class="sxs-lookup"><span data-stu-id="11748-114">Server</span></span><br/> | <span data-ttu-id="11748-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="11748-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11748-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="11748-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11748-117">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="11748-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="11748-118">Esquema mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="11748-118">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





