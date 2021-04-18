---
title: Método INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent. h)
description: SHA usa para comparar solicitudes de SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Método CompareSoHRequests NAP
- Método CompareSoHRequests NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método CompareSoHRequests
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676789"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a><span data-ttu-id="09512-106">INapSystemHealthAgentCallback:: CompareSoHRequests (método)</span><span class="sxs-lookup"><span data-stu-id="09512-106">INapSystemHealthAgentCallback::CompareSoHRequests method</span></span>

> [!Note]  
> <span data-ttu-id="09512-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="09512-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="09512-108">SHA usa el método **INapSystemHealthAgentCallback:: CompareSoHRequests** para comparar solicitudes de SOH.</span><span class="sxs-lookup"><span data-stu-id="09512-108">The **INapSystemHealthAgentCallback::CompareSoHRequests** method is used by the SHA to compare SoH requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="09512-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09512-109">Syntax</span></span>


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a><span data-ttu-id="09512-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09512-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09512-111">*LHS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09512-111">*lhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09512-112">Puntero al [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a la izquierda de la operación de comparación.</span><span class="sxs-lookup"><span data-stu-id="09512-112">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the left of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="09512-113">*RHS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09512-113">*rhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09512-114">Puntero al [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a la derecha de la operación de comparación.</span><span class="sxs-lookup"><span data-stu-id="09512-114">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the right of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="09512-115">*isEqual* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="09512-115">*isEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09512-116">Un puntero a un **valor** **booleano** que es true si *LHS* y *RHS* son semánticamente iguales y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="09512-116">A pointer to a **BOOL** that is **TRUE** if *lhs* and *rhs* are semantically equal, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09512-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09512-117">Return value</span></span>

<span data-ttu-id="09512-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="09512-118">This method can return one of these values.</span></span>



| <span data-ttu-id="09512-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="09512-119">Return code</span></span>                                                                               | <span data-ttu-id="09512-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="09512-120">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="09512-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="09512-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="09512-122">Indica que se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="09512-122">Indicates success.</span></span><br/>                         |
| <dl> <span data-ttu-id="09512-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="09512-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="09512-124">SHA no implementó el método.</span><span class="sxs-lookup"><span data-stu-id="09512-124">The method was not implemented by the SHA.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09512-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09512-125">Remarks</span></span>

<span data-ttu-id="09512-126">Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.</span><span class="sxs-lookup"><span data-stu-id="09512-126">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="09512-127">SHA debe comparar SOH y devolver **true** si SOH son semánticamente iguales.</span><span class="sxs-lookup"><span data-stu-id="09512-127">The SHA should compare the SoHs and return **TRUE** if the SoHs are semantically equal.</span></span> <span data-ttu-id="09512-128">NapAgent usa esta información para determinar si se debe iniciar un intercambio de SoH debido al cambio de estado del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="09512-128">The NapAgent uses this information to determine if an SoH exchange should be initiated due to change of state of the client machine.</span></span>

<span data-ttu-id="09512-129">Si los Sha han colocado identificadores incrementales o marcas de tiempo en su SoH, SOH puede ser semánticamente igual (es decir, pueden transmitir la misma información de estado), pero pueden ser unidireccionales por bytes.</span><span class="sxs-lookup"><span data-stu-id="09512-129">If SHAs have put incremental IDs or time-stamps into their SoH, then SoHs may be semantically equal (i.e. they may convey the same health information), but they may be byte-wise unequal.</span></span> <span data-ttu-id="09512-130">Los Sha deben implementar esta función para comprobar la igualdad semántica de SOH.</span><span class="sxs-lookup"><span data-stu-id="09512-130">SHAs should implement this function to check for semantic equality of SoHs.</span></span>

<span data-ttu-id="09512-131">Si los Sha no han colocado marcas de tiempo o identificadores en su SOH, pueden optar por no implementar esta función y devolver **e \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="09512-131">If SHAs have not put any time-stamps or Ids into their SoHs, they may choose to not implement this function and return **E\_NOTIMPL**.</span></span> <span data-ttu-id="09512-132">En este caso, NapAgent realiza una comparación de bytes en [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="09512-132">In this case, the NapAgent performs a byte-wise comparison on the [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="requirements"></a><span data-ttu-id="09512-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09512-133">Requirements</span></span>



| <span data-ttu-id="09512-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="09512-134">Requirement</span></span> | <span data-ttu-id="09512-135">Value</span><span class="sxs-lookup"><span data-stu-id="09512-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09512-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09512-136">Minimum supported client</span></span><br/> | <span data-ttu-id="09512-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="09512-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="09512-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09512-138">Minimum supported server</span></span><br/> | <span data-ttu-id="09512-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="09512-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="09512-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09512-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="09512-141"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="09512-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="09512-142">IDL</span><span class="sxs-lookup"><span data-stu-id="09512-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09512-143"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="09512-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09512-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="09512-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09512-145">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="09512-145">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> <dt>

[<span data-ttu-id="09512-146">**SoH**</span><span class="sxs-lookup"><span data-stu-id="09512-146">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





