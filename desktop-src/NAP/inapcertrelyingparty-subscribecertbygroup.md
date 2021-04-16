---
title: Método INapCertRelyingParty SubscribeCertByGroup (NapCertRelyingParty. h)
description: Se suscribe a un servidor de certificados de mantenimiento (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Método SubscribeCertByGroup NAP
- Método SubscribeCertByGroup NAP, interfaz INapCertRelyingParty
- Interfaz INapCertRelyingParty NAP, método SubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651402"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a><span data-ttu-id="33bee-106">INapCertRelyingParty:: SubscribeCertByGroup (método)</span><span class="sxs-lookup"><span data-stu-id="33bee-106">INapCertRelyingParty::SubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="33bee-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="33bee-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="33bee-108">El método **SubscribeCertByGroup** se suscribe a un servidor de certificados de mantenimiento (HCS).</span><span class="sxs-lookup"><span data-stu-id="33bee-108">The **SubscribeCertByGroup** method subscribes to a health certificate server (HCS).</span></span> <span data-ttu-id="33bee-109">El HCS ya debe estar registrado antes de suscribirse.</span><span class="sxs-lookup"><span data-stu-id="33bee-109">The HCS must already be registered before subscribing.</span></span>

## <a name="syntax"></a><span data-ttu-id="33bee-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33bee-110">Syntax</span></span>


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a><span data-ttu-id="33bee-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33bee-111">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="33bee-112">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="33bee-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33bee-113">Un [**EnforcementEntityId**](nap-datatypes.md) que contiene el identificador del cliente de cumplimiento que se suscribe.</span><span class="sxs-lookup"><span data-stu-id="33bee-113">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is subscribing.</span></span>

</dd> <dt>

<span data-ttu-id="33bee-114">*subscriberName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33bee-114">*subscriberName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33bee-115">El nombre del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="33bee-115">The name of the subscriber.</span></span>

> [!Note]  
> <span data-ttu-id="33bee-116">Actualmente, esto solo se usa para fines de registro.</span><span class="sxs-lookup"><span data-stu-id="33bee-116">This is currently only used for logging purposes.</span></span>

 

</dd> <dt>

<span data-ttu-id="33bee-117">*reservado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33bee-117">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33bee-118">Debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="33bee-118">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33bee-119">*certExists* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="33bee-119">*certExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33bee-120">Indica si el NapAgent ya mantiene un certificado de mantenimiento de este HCS y está presente en el almacén del equipo.</span><span class="sxs-lookup"><span data-stu-id="33bee-120">Indicates whether a health certificate from this HCS is already being maintained by the NapAgent and is present in the machine store.</span></span> <span data-ttu-id="33bee-121">Si es **true**, ya se está manteniendo un certificado de mantenimiento y está presente.</span><span class="sxs-lookup"><span data-stu-id="33bee-121">If **TRUE**, a health certificate is already being maintained and is present.</span></span> <span data-ttu-id="33bee-122">Si es **false**, no se mantiene actualmente un certificado de mantenimiento y está presente.</span><span class="sxs-lookup"><span data-stu-id="33bee-122">If **FALSE**, a health certificate is not currently being maintained and present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33bee-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33bee-123">Return value</span></span>

<span data-ttu-id="33bee-124">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="33bee-124">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="33bee-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="33bee-125">Return code</span></span>                                                                                     | <span data-ttu-id="33bee-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="33bee-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="33bee-127"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="33bee-127"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="33bee-128">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="33bee-128">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="33bee-129"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="33bee-129"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="33bee-130">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="33bee-130">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="33bee-131"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="33bee-131"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="33bee-132">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="33bee-132">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="33bee-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33bee-133">Requirements</span></span>



| <span data-ttu-id="33bee-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="33bee-134">Requirement</span></span> | <span data-ttu-id="33bee-135">Value</span><span class="sxs-lookup"><span data-stu-id="33bee-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33bee-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33bee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="33bee-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="33bee-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33bee-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33bee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="33bee-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="33bee-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="33bee-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33bee-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="33bee-141"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="33bee-141"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="33bee-142">IDL</span><span class="sxs-lookup"><span data-stu-id="33bee-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33bee-143"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33bee-143"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33bee-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="33bee-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33bee-145">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="33bee-145">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





