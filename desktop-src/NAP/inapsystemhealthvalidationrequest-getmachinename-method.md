---
title: Método INapSystemHealthValidationRequest GetMachineName (NapSystemHealthValidator. h)
description: Lo usan los validadores de mantenimiento del sistema (SHV) para recuperar el nombre del equipo del cliente NAP. A continuación, el SHV registra esta información.
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- Método GetMachineName NAP
- Método GetMachineName NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método GetMachineName
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1c3e264d7d2d6e4d93e3ad71d7f3adc92ff8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151228"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a><span data-ttu-id="9b39a-107">INapSystemHealthValidationRequest:: GetMachineName (método)</span><span class="sxs-lookup"><span data-stu-id="9b39a-107">INapSystemHealthValidationRequest::GetMachineName method</span></span>

> [!Note]  
> <span data-ttu-id="9b39a-108">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="9b39a-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9b39a-109">Los validadores de mantenimiento del sistema (SHV) usan el método **INapSystemHealthValidationRequest:: GetMachineName** para recuperar el nombre de equipo del cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="9b39a-109">The **INapSystemHealthValidationRequest::GetMachineName** method is used by System Health Validators (SHVs) to retrieve the machine name of the NAP client.</span></span> <span data-ttu-id="9b39a-110">A continuación, el SHV registra esta información.</span><span class="sxs-lookup"><span data-stu-id="9b39a-110">The SHV then logs this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b39a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b39a-111">Syntax</span></span>


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a><span data-ttu-id="9b39a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b39a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b39a-113">*MachineName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9b39a-113">*machineName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b39a-114">Un puntero a un puntero a una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre de equipo del cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="9b39a-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b39a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b39a-115">Return value</span></span>

<span data-ttu-id="9b39a-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="9b39a-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9b39a-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9b39a-117">Return code</span></span>                                                                                     | <span data-ttu-id="9b39a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b39a-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9b39a-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="9b39a-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9b39a-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b39a-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9b39a-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="9b39a-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9b39a-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="9b39a-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9b39a-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9b39a-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9b39a-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="9b39a-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9b39a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b39a-125">Requirements</span></span>



| <span data-ttu-id="9b39a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b39a-126">Requirement</span></span> | <span data-ttu-id="9b39a-127">Value</span><span class="sxs-lookup"><span data-stu-id="9b39a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b39a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b39a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9b39a-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9b39a-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="9b39a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b39a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9b39a-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b39a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b39a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b39a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b39a-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b39a-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b39a-134">IDL</span><span class="sxs-lookup"><span data-stu-id="9b39a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9b39a-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b39a-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="9b39a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b39a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b39a-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b39a-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="9b39a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b39a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b39a-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="9b39a-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





