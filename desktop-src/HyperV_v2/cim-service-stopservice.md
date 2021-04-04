---
description: Acelera el servicio en estado detenido.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Método StopService de la clase CIM_Service (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4eb354a48b074bad8adac4d5635e204844c31b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908097"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="46216-103">Método StopService de la clase CIM_Service (administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="46216-103">StopService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="46216-104">Acelera el servicio en estado detenido.</span><span class="sxs-lookup"><span data-stu-id="46216-104">Paces the service in the stopped state.</span></span>

> [!Note]
>
> <span data-ttu-id="46216-105">La semántica de este método se superpone con el método **RequestStateChange** que se hereda de [**\_ EnabledLogicalElement CIM**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="46216-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="46216-106">Este método se mantiene porque se ha implementado de forma generalizada y su semántica simple de "detención" es conveniente para su uso.</span><span class="sxs-lookup"><span data-stu-id="46216-106">This method is maintained because it has been widely implemented, and its simple "stop" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="46216-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46216-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="46216-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46216-108">Parameters</span></span>

<span data-ttu-id="46216-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="46216-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46216-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46216-110">Return value</span></span>

<span data-ttu-id="46216-111">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="46216-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="46216-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46216-112">Requirements</span></span>



| <span data-ttu-id="46216-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="46216-113">Requirement</span></span> | <span data-ttu-id="46216-114">Value</span><span class="sxs-lookup"><span data-stu-id="46216-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46216-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46216-115">Minimum supported client</span></span><br/> | <span data-ttu-id="46216-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="46216-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="46216-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46216-117">Minimum supported server</span></span><br/> | <span data-ttu-id="46216-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="46216-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="46216-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46216-119">Namespace</span></span><br/>                | <span data-ttu-id="46216-120">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="46216-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="46216-121">MOF</span><span class="sxs-lookup"><span data-stu-id="46216-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46216-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46216-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46216-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46216-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46216-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46216-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46216-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="46216-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46216-126">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="46216-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




