---
title: Elemento User
description: Obtenga información sobre el elemento User. Este elemento no se usa cuando se usan métodos heredados a través de las API de EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Elemento de usuario EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793923"
---
# <a name="user-element"></a><span data-ttu-id="56791-105">Elemento User</span><span class="sxs-lookup"><span data-stu-id="56791-105">User Element</span></span>

<span data-ttu-id="56791-106">El elemento **User** no se usa cuando se usan métodos heredados a través de las API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="56791-106">The **User** element is not used when using legacy methods via the EAPHost APIs.</span></span>

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="56791-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="56791-107">Child elements</span></span>



| <span data-ttu-id="56791-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="56791-108">Element</span></span>                                                  | <span data-ttu-id="56791-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="56791-109">Type</span></span> | <span data-ttu-id="56791-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="56791-110">Description</span></span>                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="56791-111">**Participante**</span><span class="sxs-lookup"><span data-stu-id="56791-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md) |      | <span data-ttu-id="56791-112">Captura la información de credenciales específica del método y el tipo de método.</span><span class="sxs-lookup"><span data-stu-id="56791-112">Captures the method type and method specific credential information.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="56791-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56791-113">Requirements</span></span>



| <span data-ttu-id="56791-114">Role</span><span class="sxs-lookup"><span data-stu-id="56791-114">Role</span></span> | <span data-ttu-id="56791-115">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="56791-115">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="56791-116">Remoto</span><span class="sxs-lookup"><span data-stu-id="56791-116">Client</span></span><br/> | <span data-ttu-id="56791-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="56791-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="56791-118">Servidor</span><span class="sxs-lookup"><span data-stu-id="56791-118">Server</span></span><br/> | <span data-ttu-id="56791-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="56791-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56791-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="56791-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56791-121">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="56791-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="56791-122">Esquema eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="56791-122">eapuserpropertiesv1 Schema</span></span>](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





