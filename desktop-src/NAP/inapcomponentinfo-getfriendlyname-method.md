---
title: Método INapComponentInfo GetFriendlyName (NapCommon. h)
description: Lo usa el sistema NAP para obtener el nombre descriptivo de un cliente de mantenimiento.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Método GetFriendlyName NAP
- Método GetFriendlyName NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetFriendlyName
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848f8fb8365f91bceb5a44c498578f04a1776b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492808"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a><span data-ttu-id="417c1-106">INapComponentInfo:: GetFriendlyName (método)</span><span class="sxs-lookup"><span data-stu-id="417c1-106">INapComponentInfo::GetFriendlyName method</span></span>

> [!Note]  
> <span data-ttu-id="417c1-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="417c1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="417c1-108">El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: GetFriendlyName** para obtener el nombre descriptivo de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="417c1-108">The **INapComponentInfo::GetFriendlyName** callback method is used by the NAP System to get the friendly name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="417c1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="417c1-109">Syntax</span></span>


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="417c1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="417c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="417c1-111">*friendlyName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="417c1-111">*friendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="417c1-112">Un puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso del nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="417c1-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="417c1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="417c1-113">Return value</span></span>

<span data-ttu-id="417c1-114">Devuelva uno de estos códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="417c1-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="417c1-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="417c1-115">Return code</span></span>                                                                                     | <span data-ttu-id="417c1-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="417c1-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="417c1-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="417c1-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="417c1-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="417c1-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="417c1-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="417c1-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="417c1-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="417c1-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="417c1-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="417c1-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="417c1-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="417c1-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="417c1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="417c1-123">Requirements</span></span>



| <span data-ttu-id="417c1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="417c1-124">Requirement</span></span> | <span data-ttu-id="417c1-125">Value</span><span class="sxs-lookup"><span data-stu-id="417c1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="417c1-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="417c1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="417c1-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="417c1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="417c1-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="417c1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="417c1-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="417c1-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="417c1-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="417c1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="417c1-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="417c1-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="417c1-132">IDL</span><span class="sxs-lookup"><span data-stu-id="417c1-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="417c1-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="417c1-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="417c1-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="417c1-134">See also</span></span>

<dl> <span data-ttu-id="417c1-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="417c1-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="417c1-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="417c1-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





