---
description: Coloca el servicio en estado Iniciado.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Método StartService de la clase CIM_Service (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 73b89f7fc789639fb45acbde61da4c7962650177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686901"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="28f6d-103">Método StartService de la clase CIM_Service (administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="28f6d-103">StartService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="28f6d-104">Coloca el servicio en estado Iniciado.</span><span class="sxs-lookup"><span data-stu-id="28f6d-104">Places the service in the started state.</span></span>

> [!Note]
>
> <span data-ttu-id="28f6d-105">La semántica de este método se superpone con el método **RequestStateChange** que se hereda de [**\_ EnabledLogicalElement CIM**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="28f6d-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="28f6d-106">Este método se mantiene porque se ha implementado ampliamente y su semántica simple de "Inicio" es conveniente para su uso.</span><span class="sxs-lookup"><span data-stu-id="28f6d-106">This method is maintained because it has been widely implemented, and its simple "start" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="28f6d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28f6d-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="28f6d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28f6d-108">Parameters</span></span>

<span data-ttu-id="28f6d-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="28f6d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28f6d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28f6d-110">Return value</span></span>

<span data-ttu-id="28f6d-111">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="28f6d-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="28f6d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28f6d-112">Requirements</span></span>



| <span data-ttu-id="28f6d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="28f6d-113">Requirement</span></span> | <span data-ttu-id="28f6d-114">Value</span><span class="sxs-lookup"><span data-stu-id="28f6d-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28f6d-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28f6d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="28f6d-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="28f6d-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="28f6d-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28f6d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="28f6d-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="28f6d-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="28f6d-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="28f6d-119">Namespace</span></span><br/>                | <span data-ttu-id="28f6d-120">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="28f6d-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="28f6d-121">MOF</span><span class="sxs-lookup"><span data-stu-id="28f6d-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28f6d-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28f6d-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="28f6d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28f6d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28f6d-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28f6d-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="28f6d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="28f6d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28f6d-126">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="28f6d-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




