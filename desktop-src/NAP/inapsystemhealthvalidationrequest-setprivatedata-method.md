---
title: Método INapSystemHealthValidationRequest SetPrivateData (NapSystemHealthValidator. h)
description: Permite que NapServer almacene información de estado.
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- Método SetPrivateData NAP
- Método SetPrivateData NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método SetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da50ca236c08388632e17916decee162b3b71743
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802816"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a><span data-ttu-id="d368f-106">INapSystemHealthValidationRequest:: SetPrivateData (método)</span><span class="sxs-lookup"><span data-stu-id="d368f-106">INapSystemHealthValidationRequest::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="d368f-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="d368f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d368f-108">El método **INapSystemHealthValidationRequest:: SetPrivateData** permite que NapServer almacene información de estado.</span><span class="sxs-lookup"><span data-stu-id="d368f-108">The **INapSystemHealthValidationRequest::SetPrivateData** method allows the NapServer to store state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d368f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d368f-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="d368f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d368f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d368f-111">*privateData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d368f-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d368f-112">Un puntero a un BLOB de datos [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que contiene la información de estado opaca.</span><span class="sxs-lookup"><span data-stu-id="d368f-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that contains the opaque state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d368f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d368f-113">Return value</span></span>

<span data-ttu-id="d368f-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="d368f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d368f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d368f-115">Return code</span></span>                                                                                     | <span data-ttu-id="d368f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d368f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d368f-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="d368f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d368f-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="d368f-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d368f-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d368f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d368f-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="d368f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d368f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d368f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d368f-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="d368f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d368f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d368f-123">Remarks</span></span>

<span data-ttu-id="d368f-124">Solo NapServer puede interpretar el BLOB de datos.</span><span class="sxs-lookup"><span data-stu-id="d368f-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="d368f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d368f-125">Requirements</span></span>



| <span data-ttu-id="d368f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d368f-126">Requirement</span></span> | <span data-ttu-id="d368f-127">Value</span><span class="sxs-lookup"><span data-stu-id="d368f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d368f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d368f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d368f-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d368f-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="d368f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d368f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d368f-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d368f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d368f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d368f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d368f-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="d368f-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="d368f-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d368f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d368f-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d368f-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="d368f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d368f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d368f-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d368f-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="d368f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d368f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d368f-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="d368f-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





