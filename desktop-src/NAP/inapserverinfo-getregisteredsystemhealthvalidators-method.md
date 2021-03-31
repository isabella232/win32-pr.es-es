---
title: Método INapServerInfo GetRegisteredSystemHealthValidators (NapServerManagement. h)
description: Recupera una lista de SHV registrados.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Método GetRegisteredSystemHealthValidators NAP
- Método GetRegisteredSystemHealthValidators NAP, interfaz INapServerInfo
- Interfaz INapServerInfo NAP, método GetRegisteredSystemHealthValidators
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079639"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a><span data-ttu-id="39455-106">INapServerInfo:: GetRegisteredSystemHealthValidators (método)</span><span class="sxs-lookup"><span data-stu-id="39455-106">INapServerInfo::GetRegisteredSystemHealthValidators method</span></span>

> [!Note]  
> <span data-ttu-id="39455-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="39455-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="39455-108">El método **INapServerInfo:: GetRegisteredSystemHealthValidators** recupera una lista de SHV registrados.</span><span class="sxs-lookup"><span data-stu-id="39455-108">The **INapServerInfo::GetRegisteredSystemHealthValidators** method retrieves a list of registered SHVs.</span></span>

## <a name="syntax"></a><span data-ttu-id="39455-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39455-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a><span data-ttu-id="39455-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39455-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39455-111">*recuento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39455-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39455-112">Un puntero a un [**SystemHealthEntityCount**](nap-type-constants.md) que contiene el número de SHV registrados.</span><span class="sxs-lookup"><span data-stu-id="39455-112">A pointer to a [**SystemHealthEntityCount**](nap-type-constants.md) that contains the number of registered SHVs.</span></span>

</dd> <dt>

<span data-ttu-id="39455-113">*Validadores* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39455-113">*validators* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39455-114">Un puntero a un puntero a una estructura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro de SHV.</span><span class="sxs-lookup"><span data-stu-id="39455-114">A pointer to a pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="39455-115">*validatorClsids* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39455-115">*validatorClsids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39455-116">Puntero a una matriz de identificadores de los SHV registrados.</span><span class="sxs-lookup"><span data-stu-id="39455-116">Pointer to an array of IDs for the registered SHVs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39455-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39455-117">Return value</span></span>

<span data-ttu-id="39455-118">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="39455-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="39455-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="39455-119">Return code</span></span>                                                                                     | <span data-ttu-id="39455-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="39455-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="39455-121"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="39455-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="39455-122">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="39455-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="39455-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="39455-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="39455-124">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="39455-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="39455-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="39455-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="39455-126">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="39455-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39455-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39455-127">Requirements</span></span>



| <span data-ttu-id="39455-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="39455-128">Requirement</span></span> | <span data-ttu-id="39455-129">Value</span><span class="sxs-lookup"><span data-stu-id="39455-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39455-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39455-130">Minimum supported client</span></span><br/> | <span data-ttu-id="39455-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="39455-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="39455-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39455-132">Minimum supported server</span></span><br/> | <span data-ttu-id="39455-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="39455-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39455-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39455-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="39455-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="39455-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="39455-136">IDL</span><span class="sxs-lookup"><span data-stu-id="39455-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39455-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39455-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="39455-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39455-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39455-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39455-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="39455-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="39455-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39455-141">**NapComponentRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="39455-141">**NapComponentRegistrationInfo**</span></span>](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[<span data-ttu-id="39455-142">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="39455-142">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





