---
title: Elemento EapType (propiedad de conexión del esquema V1)
description: Obtenga información sobre el elemento EapType. Este elemento captura la configuración específica del método dentro del elemento EAP. | Elemento EapType (propiedad de conexión del esquema V1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
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
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820570"
---
# <a name="eaptype-element-v1-schema-connection-property"></a><span data-ttu-id="343d1-106">Elemento EapType (propiedad de conexión del esquema V1)</span><span class="sxs-lookup"><span data-stu-id="343d1-106">EapType Element (v1 schema connection property)</span></span>

<span data-ttu-id="343d1-107">El elemento **EapType** captura la configuración específica del método dentro del elemento EAP.</span><span class="sxs-lookup"><span data-stu-id="343d1-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="343d1-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="343d1-108">Remarks</span></span>

<span data-ttu-id="343d1-109">El elemento **EapType** es abstracto; cada método debe definir y usar un elemento derivado en los documentos de instancia.</span><span class="sxs-lookup"><span data-stu-id="343d1-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="343d1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="343d1-110">Requirements</span></span>



| <span data-ttu-id="343d1-111">Role</span><span class="sxs-lookup"><span data-stu-id="343d1-111">Role</span></span> | <span data-ttu-id="343d1-112">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="343d1-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="343d1-113">Remoto</span><span class="sxs-lookup"><span data-stu-id="343d1-113">Client</span></span><br/> | <span data-ttu-id="343d1-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="343d1-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="343d1-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="343d1-115">Server</span></span><br/> | <span data-ttu-id="343d1-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="343d1-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="343d1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="343d1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="343d1-118">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="343d1-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="343d1-119">Esquema baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="343d1-119">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





