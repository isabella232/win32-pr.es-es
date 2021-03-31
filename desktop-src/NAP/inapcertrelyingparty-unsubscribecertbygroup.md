---
title: Método INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty. h)
description: Cancela la suscripción de un servidor de certificados de mantenimiento (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Método UnSubscribeCertByGroup NAP
- Método UnSubscribeCertByGroup NAP, interfaz INapCertRelyingParty
- Interfaz INapCertRelyingParty NAP, método UnSubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996534"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a><span data-ttu-id="dddc4-106">INapCertRelyingParty:: UnSubscribeCertByGroup (método)</span><span class="sxs-lookup"><span data-stu-id="dddc4-106">INapCertRelyingParty::UnSubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="dddc4-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="dddc4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dddc4-108">El método **UnSubscribeCertByGroup** cancela la suscripción de un servidor de certificados de mantenimiento (HCS).</span><span class="sxs-lookup"><span data-stu-id="dddc4-108">The **UnSubscribeCertByGroup** method unsubscribes from a health certificate server (HCS).</span></span>

## <a name="syntax"></a><span data-ttu-id="dddc4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dddc4-109">Syntax</span></span>


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a><span data-ttu-id="dddc4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dddc4-110">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="dddc4-111">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="dddc4-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dddc4-112">Un [**EnforcementEntityId**](nap-datatypes.md) que contiene el identificador del cliente de cumplimiento que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="dddc4-112">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is unsubscribing.</span></span>

</dd> <dt>

 <span data-ttu-id="dddc4-113">*reservado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dddc4-113">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dddc4-114">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="dddc4-114">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dddc4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dddc4-115">Return value</span></span>

<span data-ttu-id="dddc4-116">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="dddc4-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="dddc4-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dddc4-117">Return code</span></span>                                                                                     | <span data-ttu-id="dddc4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dddc4-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="dddc4-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="dddc4-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="dddc4-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dddc4-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="dddc4-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="dddc4-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="dddc4-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="dddc4-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="dddc4-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dddc4-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="dddc4-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="dddc4-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dddc4-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dddc4-125">Remarks</span></span>

<span data-ttu-id="dddc4-126">Si no hay ningún otro suscriptor al HCS, el NapAgent eliminará los certificados de mantenimiento correspondientes del almacén del equipo local.</span><span class="sxs-lookup"><span data-stu-id="dddc4-126">If there are no other subscribers to the HCS, the NapAgent will delete the corresponding health certificates from the local machine store.</span></span>

<span data-ttu-id="dddc4-127">Antes de llamar a este método, llame a [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span><span class="sxs-lookup"><span data-stu-id="dddc4-127">Before calling this method, call [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dddc4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dddc4-128">Requirements</span></span>



| <span data-ttu-id="dddc4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dddc4-129">Requirement</span></span> | <span data-ttu-id="dddc4-130">Value</span><span class="sxs-lookup"><span data-stu-id="dddc4-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dddc4-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dddc4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dddc4-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dddc4-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dddc4-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dddc4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dddc4-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dddc4-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dddc4-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dddc4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dddc4-136"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="dddc4-136"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="dddc4-137">IDL</span><span class="sxs-lookup"><span data-stu-id="dddc4-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dddc4-138"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dddc4-138"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dddc4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="dddc4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dddc4-140">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="dddc4-140">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





