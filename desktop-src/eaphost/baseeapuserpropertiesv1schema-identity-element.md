---
title: Elemento Identity
description: Obtenga información sobre el elemento de identidad de EAPHost. Este elemento captura la identidad utilizada para la autenticación.
ms.assetid: 464979f0-6a2b-43e7-a207-2fbd1e2e5f51
keywords:
- Elemento Identity EAPHost
topic_type:
- apiref
api_name:
- Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 485d576155d5ac63df2776016f3aafabf8c18c25
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488302"
---
# <a name="identity-element"></a><span data-ttu-id="cf7fc-105">Elemento Identity</span><span class="sxs-lookup"><span data-stu-id="cf7fc-105">Identity Element</span></span>

<span data-ttu-id="cf7fc-106">El elemento **Identity** captura la identidad utilizada para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="cf7fc-106">The **Identity** element captures the identity used for authentication.</span></span>

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a><span data-ttu-id="cf7fc-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf7fc-107">Remarks</span></span>

<span data-ttu-id="cf7fc-108">El elemento **Identity** es abstracto; cada método debe definir y usar un elemento derivado en los documentos de instancia.</span><span class="sxs-lookup"><span data-stu-id="cf7fc-108">The **Identity** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf7fc-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf7fc-109">Requirements</span></span>



| <span data-ttu-id="cf7fc-110">Role</span><span class="sxs-lookup"><span data-stu-id="cf7fc-110">Role</span></span> | <span data-ttu-id="cf7fc-111">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="cf7fc-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="cf7fc-112">Remoto</span><span class="sxs-lookup"><span data-stu-id="cf7fc-112">Client</span></span><br/> | <span data-ttu-id="cf7fc-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf7fc-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf7fc-114">Servidor</span><span class="sxs-lookup"><span data-stu-id="cf7fc-114">Server</span></span><br/> | <span data-ttu-id="cf7fc-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf7fc-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf7fc-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf7fc-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf7fc-117">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="cf7fc-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="cf7fc-118">Esquema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cf7fc-118">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





