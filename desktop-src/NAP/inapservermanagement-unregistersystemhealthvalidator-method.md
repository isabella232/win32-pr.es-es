---
title: Método INapServerManagement UnregisterSystemHealthValidator (NapServerManagement. h)
description: Se usa para anular el registro de un SHV con el servidor NAP.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Método UnregisterSystemHealthValidator NAP
- Método UnregisterSystemHealthValidator NAP, interfaz INapServerManagement
- Interfaz INapServerManagement NAP, método UnregisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535014"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a><span data-ttu-id="b4421-106">INapServerManagement:: UnregisterSystemHealthValidator (método)</span><span class="sxs-lookup"><span data-stu-id="b4421-106">INapServerManagement::UnregisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="b4421-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b4421-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b4421-108">El método **INapServerManagement:: UnregisterSystemHealthValidator** se usa para anular el registro de un SHV con el servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="b4421-108">The **INapServerManagement::UnregisterSystemHealthValidator** method is used to unregister an SHV with the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4421-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4421-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="b4421-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4421-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4421-111">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b4421-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4421-112">[**SystemHealthEntityId**](nap-type-constants.md) que contiene el identificador único del SHV cuyo registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="b4421-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4421-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4421-113">Return value</span></span>

<span data-ttu-id="b4421-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="b4421-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b4421-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b4421-115">Return code</span></span>                                                                                     | <span data-ttu-id="b4421-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4421-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4421-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="b4421-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b4421-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="b4421-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b4421-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b4421-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b4421-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="b4421-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b4421-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b4421-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b4421-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b4421-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4421-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4421-123">Remarks</span></span>

<span data-ttu-id="b4421-124">Si hay llamadas asincrónicas pendientes en el SHV, se completarán en un momento posterior y se descartarán.</span><span class="sxs-lookup"><span data-stu-id="b4421-124">If there are any asynchronous calls pending on the SHV, they will complete at a later time and will be discarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4421-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4421-125">Requirements</span></span>



| <span data-ttu-id="b4421-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4421-126">Requirement</span></span> | <span data-ttu-id="b4421-127">Value</span><span class="sxs-lookup"><span data-stu-id="b4421-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4421-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4421-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b4421-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b4421-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="b4421-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4421-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b4421-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4421-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b4421-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4421-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4421-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4421-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4421-134">IDL</span><span class="sxs-lookup"><span data-stu-id="b4421-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4421-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4421-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="b4421-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4421-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4421-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4421-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="b4421-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4421-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4421-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="b4421-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





