---
title: Elemento EapType (propiedades de usuario base)
description: Obtenga información sobre el elemento EapType. Este elemento captura la configuración específica del método dentro del elemento EAP. | Elemento EapType (propiedades de usuario base)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
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
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717493"
---
# <a name="eaptype-element-base-user-properties"></a><span data-ttu-id="d0be9-106">Elemento EapType (propiedades de usuario base)</span><span class="sxs-lookup"><span data-stu-id="d0be9-106">EapType element (base user properties)</span></span>

<span data-ttu-id="d0be9-107">El elemento **EapType** captura la configuración específica del método dentro del elemento EAP.</span><span class="sxs-lookup"><span data-stu-id="d0be9-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="d0be9-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0be9-108">Remarks</span></span>

<span data-ttu-id="d0be9-109">El elemento **EapType** es abstracto; cada método debe definir y usar un elemento derivado en los documentos de instancia.</span><span class="sxs-lookup"><span data-stu-id="d0be9-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0be9-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0be9-110">Requirements</span></span>



| <span data-ttu-id="d0be9-111">Role</span><span class="sxs-lookup"><span data-stu-id="d0be9-111">Role</span></span> | <span data-ttu-id="d0be9-112">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d0be9-112">Minimum supported OS version</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0be9-113">Remoto</span><span class="sxs-lookup"><span data-stu-id="d0be9-113">Client</span></span><br/> | <span data-ttu-id="d0be9-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d0be9-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d0be9-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="d0be9-115">Server</span></span><br/> | <span data-ttu-id="d0be9-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0be9-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0be9-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0be9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0be9-118">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="d0be9-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d0be9-119">Esquema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="d0be9-119">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





