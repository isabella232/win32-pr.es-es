---
title: Método INapCertRelyingParty GetSubscribedRelyingParties (NapCertRelyingParty. h)
description: Obtiene una lista de usuarios de confianza que se han suscrito.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Método GetSubscribedRelyingParties NAP
- Método GetSubscribedRelyingParties NAP, interfaz INapCertRelyingParty
- Interfaz INapCertRelyingParty NAP, método GetSubscribedRelyingParties
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489382"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a><span data-ttu-id="a64df-106">INapCertRelyingParty:: GetSubscribedRelyingParties (método)</span><span class="sxs-lookup"><span data-stu-id="a64df-106">INapCertRelyingParty::GetSubscribedRelyingParties method</span></span>

> [!Note]  
> <span data-ttu-id="a64df-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a64df-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a64df-108">El método **GetSubscribedRelyingParties** obtiene una lista de usuarios de confianza que se han suscrito.</span><span class="sxs-lookup"><span data-stu-id="a64df-108">The **GetSubscribedRelyingParties** method gets a list of relying parties that have subscribed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64df-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a64df-109">Syntax</span></span>


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a><span data-ttu-id="a64df-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a64df-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a64df-111">*recuento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a64df-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a64df-112">Un puntero a un [**EnforcementEntityCount**](nap-datatypes.md) que contiene el número de usuarios de confianza suscritos.</span><span class="sxs-lookup"><span data-stu-id="a64df-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of subscribed relying parties.</span></span>

</dd> <dt>

<span data-ttu-id="a64df-113">*relyingParties* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a64df-113">*relyingParties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a64df-114">Un puntero a un puntero a un [**EnforcementEntityId**](nap-datatypes.md) que contiene la lista de usuarios de confianza suscritos.</span><span class="sxs-lookup"><span data-stu-id="a64df-114">A pointer to a pointer to an [**EnforcementEntityId**](nap-datatypes.md) that contains the list of subscribed relying parties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a64df-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a64df-115">Return value</span></span>

<span data-ttu-id="a64df-116">Devuelve uno de los siguientes códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="a64df-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="a64df-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a64df-117">Return code</span></span>                                                                                     | <span data-ttu-id="a64df-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a64df-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a64df-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="a64df-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a64df-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a64df-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="a64df-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a64df-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a64df-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="a64df-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a64df-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a64df-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a64df-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a64df-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a64df-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a64df-125">Remarks</span></span>

<span data-ttu-id="a64df-126">El autor de la llamada debe liberar el parámetro *relyingParties* mediante **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="a64df-126">The caller must free the *relyingParties* parameter using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a64df-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a64df-127">Requirements</span></span>



| <span data-ttu-id="a64df-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a64df-128">Requirement</span></span> | <span data-ttu-id="a64df-129">Value</span><span class="sxs-lookup"><span data-stu-id="a64df-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64df-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a64df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a64df-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a64df-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a64df-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a64df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a64df-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a64df-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a64df-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a64df-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a64df-135"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="a64df-135"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="a64df-136">IDL</span><span class="sxs-lookup"><span data-stu-id="a64df-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a64df-137"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a64df-137"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a64df-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a64df-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64df-139">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="a64df-139">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





