---
title: Elemento EAP (propiedades de conexión)
description: Obtenga información sobre el elemento EAP. Este elemento captura el tipo de método seleccionado y la configuración específica del método. | Elemento EAP (propiedades de conexión)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
keywords:
- Elemento EAP EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698066"
---
# <a name="eap-element-connection-properties"></a><span data-ttu-id="78cff-106">Elemento EAP (propiedades de conexión)</span><span class="sxs-lookup"><span data-stu-id="78cff-106">Eap Element (connection properties)</span></span>

<span data-ttu-id="78cff-107">El elemento **EAP** captura el tipo de método seleccionado y la configuración específica del método.</span><span class="sxs-lookup"><span data-stu-id="78cff-107">The **Eap** element captures the method type selected and method-specific configuration.</span></span>

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="78cff-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78cff-108">Remarks</span></span>

<span data-ttu-id="78cff-109">El método puede definir los elementos constituyentes dentro del elemento **EAP** .</span><span class="sxs-lookup"><span data-stu-id="78cff-109">The method can define the constituent elements inside the **Eap** element.</span></span> <span data-ttu-id="78cff-110">El método también realiza la validación de esquemas en los elementos de **EAP**.</span><span class="sxs-lookup"><span data-stu-id="78cff-110">The method also performs schema validation on the elements in **Eap**.</span></span>

## <a name="requirements"></a><span data-ttu-id="78cff-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78cff-111">Requirements</span></span>



| <span data-ttu-id="78cff-112">Role</span><span class="sxs-lookup"><span data-stu-id="78cff-112">Role</span></span> | <span data-ttu-id="78cff-113">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="78cff-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="78cff-114">Remoto</span><span class="sxs-lookup"><span data-stu-id="78cff-114">Client</span></span><br/> | <span data-ttu-id="78cff-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="78cff-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78cff-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="78cff-116">Server</span></span><br/> | <span data-ttu-id="78cff-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="78cff-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78cff-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="78cff-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78cff-119">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="78cff-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="78cff-120">Esquema baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="78cff-120">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





