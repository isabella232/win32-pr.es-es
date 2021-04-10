---
title: Método INapServerManagement RegisterSystemHealthValidator (NapServerManagement. h)
description: Registra un SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Método RegisterSystemHealthValidator NAP
- Método RegisterSystemHealthValidator NAP, interfaz INapServerManagement
- Interfaz INapServerManagement NAP, método RegisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274559"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a><span data-ttu-id="5be10-106">INapServerManagement:: RegisterSystemHealthValidator (método)</span><span class="sxs-lookup"><span data-stu-id="5be10-106">INapServerManagement::RegisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="5be10-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5be10-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5be10-108">El método **INapServerManagement:: RegisterSystemHealthValidator** registra un SHV.</span><span class="sxs-lookup"><span data-stu-id="5be10-108">The **INapServerManagement::RegisterSystemHealthValidator** method registers an SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be10-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5be10-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a><span data-ttu-id="5be10-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5be10-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5be10-111">*validador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5be10-111">*validator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be10-112">Puntero a una estructura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contiene la información de registro de SHV.</span><span class="sxs-lookup"><span data-stu-id="5be10-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="5be10-113">*validatorClsid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5be10-113">*validatorClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be10-114">Puntero al CLSID de la clase COM que implementa la interfaz [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) .</span><span class="sxs-lookup"><span data-stu-id="5be10-114">A pointer to the CLSID of the COM class that implements the [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5be10-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5be10-115">Return value</span></span>

<span data-ttu-id="5be10-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="5be10-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5be10-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5be10-117">Return code</span></span>                                                                                            | <span data-ttu-id="5be10-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="5be10-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5be10-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="5be10-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="5be10-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="5be10-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5be10-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5be10-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="5be10-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="5be10-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5be10-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5be10-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="5be10-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="5be10-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5be10-125"><dt>**\_ \_ identificador conflictivo de NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="5be10-125"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="5be10-126">El ID. de SHV ya está registrado.</span><span class="sxs-lookup"><span data-stu-id="5be10-126">SHV id is already registered.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="5be10-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5be10-127">Requirements</span></span>



| <span data-ttu-id="5be10-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5be10-128">Requirement</span></span> | <span data-ttu-id="5be10-129">Value</span><span class="sxs-lookup"><span data-stu-id="5be10-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5be10-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5be10-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5be10-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5be10-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="5be10-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5be10-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5be10-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5be10-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5be10-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5be10-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5be10-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="5be10-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="5be10-136">IDL</span><span class="sxs-lookup"><span data-stu-id="5be10-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5be10-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5be10-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="5be10-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5be10-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5be10-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5be10-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="5be10-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5be10-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be10-141">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="5be10-141">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





