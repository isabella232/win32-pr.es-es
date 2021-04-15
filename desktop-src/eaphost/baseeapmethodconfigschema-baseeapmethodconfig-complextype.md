---
title: Tipo complejo de BaseEapMethodConfig
description: Obtenga información sobre el tipo complejo de BaseEapMethodConfig. Este tipo es un elemento de marcador de posición para la configuración del método.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- Tipo complejo BaseEapMethodConfig EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421429"
---
# <a name="baseeapmethodconfig-complex-type"></a><span data-ttu-id="d5723-105">Tipo complejo de BaseEapMethodConfig</span><span class="sxs-lookup"><span data-stu-id="d5723-105">BaseEapMethodConfig Complex Type</span></span>

<span data-ttu-id="d5723-106">El tipo complejo de **BaseEapMethodConfig** es un elemento de marcador de posición para la configuración del método.</span><span class="sxs-lookup"><span data-stu-id="d5723-106">The **BaseEapMethodConfig** complex type is a placeholder element for the method configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="d5723-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5723-107">Remarks</span></span>

<span data-ttu-id="d5723-108">El método EAP realiza la validación del esquema en el contenido del elemento **BaseEapMethodConfig** .</span><span class="sxs-lookup"><span data-stu-id="d5723-108">The EAP method performs schema validation on the contents of the **BaseEapMethodConfig** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5723-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5723-109">Requirements</span></span>



| <span data-ttu-id="d5723-110">Role</span><span class="sxs-lookup"><span data-stu-id="d5723-110">Role</span></span> | <span data-ttu-id="d5723-111">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d5723-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="d5723-112">Remoto</span><span class="sxs-lookup"><span data-stu-id="d5723-112">Client</span></span><br/> | <span data-ttu-id="d5723-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5723-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d5723-114">Servidor</span><span class="sxs-lookup"><span data-stu-id="d5723-114">Server</span></span><br/> | <span data-ttu-id="d5723-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5723-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5723-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5723-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5723-117">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="d5723-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d5723-118">Esquema baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="d5723-118">baseeapmethodconfig Schema</span></span>](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





