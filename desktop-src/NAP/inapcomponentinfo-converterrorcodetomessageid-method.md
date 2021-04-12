---
title: Método INapComponentInfo ConvertErrorCodeToMessageId (NapCommon. h)
description: Lo usa el sistema NAP para solicitar al cliente de mantenimiento que convierta un código de error HRESULT en un ID. de mensaje.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Método ConvertErrorCodeToMessageId NAP
- Método ConvertErrorCodeToMessageId NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método ConvertErrorCodeToMessageId
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492809"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a><span data-ttu-id="28622-106">INapComponentInfo:: ConvertErrorCodeToMessageId (método)</span><span class="sxs-lookup"><span data-stu-id="28622-106">INapComponentInfo::ConvertErrorCodeToMessageId method</span></span>

> [!Note]  
> <span data-ttu-id="28622-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="28622-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="28622-108">El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: ConvertErrorCodeToMessageId** para solicitar al cliente de mantenimiento que convierta un código de error HRESULT en un identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="28622-108">The **INapComponentInfo::ConvertErrorCodeToMessageId** callback method is used by the NAP System to request the health client convert an HRESULT error code into a message ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="28622-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28622-109">Syntax</span></span>


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a><span data-ttu-id="28622-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28622-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28622-111">*ErrorCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28622-111">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28622-112">[**Código de error**](nap-error-constants.md) del sistema NAP que se va a convertir en **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="28622-112">The [**error code**](nap-error-constants.md) from the NAP System that is to be converted into a **MessageId**.</span></span>

</dd> <dt>

<span data-ttu-id="28622-113">*msgId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28622-113">*msgId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28622-114">Un puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la cadena localizada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="28622-114">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the corresponding localized string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28622-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28622-115">Return value</span></span>

<span data-ttu-id="28622-116">Devuelva uno de estos códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="28622-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="28622-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="28622-117">Return code</span></span>                                                                                     | <span data-ttu-id="28622-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="28622-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="28622-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="28622-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="28622-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="28622-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="28622-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="28622-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="28622-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="28622-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="28622-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="28622-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="28622-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="28622-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28622-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28622-125">Remarks</span></span>

<span data-ttu-id="28622-126">El sistema NAP usa el **MessageId** devuelto para recuperar una cadena traducida.</span><span class="sxs-lookup"><span data-stu-id="28622-126">The returned **MessageId** is used by the NAP System to retrieve a localized string.</span></span>

## <a name="requirements"></a><span data-ttu-id="28622-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28622-127">Requirements</span></span>



| <span data-ttu-id="28622-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="28622-128">Requirement</span></span> | <span data-ttu-id="28622-129">Value</span><span class="sxs-lookup"><span data-stu-id="28622-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28622-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28622-130">Minimum supported client</span></span><br/> | <span data-ttu-id="28622-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="28622-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="28622-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28622-132">Minimum supported server</span></span><br/> | <span data-ttu-id="28622-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="28622-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="28622-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28622-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="28622-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="28622-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="28622-136">IDL</span><span class="sxs-lookup"><span data-stu-id="28622-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28622-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28622-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28622-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="28622-138">See also</span></span>

<dl> <span data-ttu-id="28622-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="28622-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="28622-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="28622-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





