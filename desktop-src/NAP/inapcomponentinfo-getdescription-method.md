---
title: Método GetDescription INapComponentInfo (NapCommon. h)
description: Lo usa el sistema NAP para obtener la descripción de un cliente de mantenimiento.
ms.assetid: f8d1d5ea-0de6-426d-90eb-b035b5bd0bfd
keywords:
- Método GetDescription NAP
- Método GetDescription NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetDescription
topic_type:
- apiref
api_name:
- INapComponentInfo.GetDescription
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499aee6f7805925cc68c08b580db7b1b72763165
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665927"
---
# <a name="inapcomponentinfogetdescription-method"></a><span data-ttu-id="16a7b-106">INapComponentInfo:: GetDescription (método)</span><span class="sxs-lookup"><span data-stu-id="16a7b-106">INapComponentInfo::GetDescription method</span></span>

> [!Note]  
> <span data-ttu-id="16a7b-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="16a7b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="16a7b-108">El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: getDescription** para obtener la descripción de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="16a7b-108">The **INapComponentInfo::GetDescription** callback method is used by the NAP System to get the description of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="16a7b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16a7b-109">Syntax</span></span>


```C++
HRESULT GetDescription(
  [out] MessageId *description
);
```



## <a name="parameters"></a><span data-ttu-id="16a7b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16a7b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16a7b-111">*Descripción* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="16a7b-111">*description* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16a7b-112">Un puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la descripción.</span><span class="sxs-lookup"><span data-stu-id="16a7b-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16a7b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16a7b-113">Return value</span></span>

<span data-ttu-id="16a7b-114">Devuelva uno de estos códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="16a7b-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="16a7b-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="16a7b-115">Return code</span></span>                                                                                     | <span data-ttu-id="16a7b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="16a7b-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="16a7b-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="16a7b-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="16a7b-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="16a7b-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="16a7b-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="16a7b-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="16a7b-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="16a7b-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="16a7b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="16a7b-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="16a7b-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="16a7b-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="16a7b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16a7b-123">Requirements</span></span>



| <span data-ttu-id="16a7b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="16a7b-124">Requirement</span></span> | <span data-ttu-id="16a7b-125">Value</span><span class="sxs-lookup"><span data-stu-id="16a7b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16a7b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16a7b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="16a7b-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="16a7b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="16a7b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16a7b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="16a7b-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="16a7b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="16a7b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16a7b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="16a7b-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="16a7b-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="16a7b-132">IDL</span><span class="sxs-lookup"><span data-stu-id="16a7b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="16a7b-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="16a7b-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16a7b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="16a7b-134">See also</span></span>

<dl> <span data-ttu-id="16a7b-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="16a7b-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="16a7b-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="16a7b-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





