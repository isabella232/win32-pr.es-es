---
title: Método GetVersion de INapComponentInfo (NapCommon. h)
description: Lo usa el sistema NAP para obtener la versión de un cliente de mantenimiento.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- GetVersion (método) NAP
- Método GetVersion NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetVersion
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535535"
---
# <a name="inapcomponentinfogetversion-method"></a><span data-ttu-id="82797-106">INapComponentInfo:: GetVersion (método)</span><span class="sxs-lookup"><span data-stu-id="82797-106">INapComponentInfo::GetVersion method</span></span>

> [!Note]  
> <span data-ttu-id="82797-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="82797-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="82797-108">El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: GetVersion** para obtener la versión de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="82797-108">The **INapComponentInfo::GetVersion** callback method is used by the NAP System to get the version of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="82797-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82797-109">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a><span data-ttu-id="82797-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82797-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82797-111">*versión* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="82797-111">*version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82797-112">Un puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso de la versión.</span><span class="sxs-lookup"><span data-stu-id="82797-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82797-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82797-113">Return value</span></span>

<span data-ttu-id="82797-114">Devuelva uno de estos códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="82797-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="82797-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="82797-115">Return code</span></span>                                                                                     | <span data-ttu-id="82797-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="82797-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="82797-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="82797-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="82797-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="82797-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="82797-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="82797-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="82797-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="82797-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="82797-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82797-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="82797-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="82797-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="82797-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82797-123">Requirements</span></span>



| <span data-ttu-id="82797-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="82797-124">Requirement</span></span> | <span data-ttu-id="82797-125">Value</span><span class="sxs-lookup"><span data-stu-id="82797-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82797-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82797-126">Minimum supported client</span></span><br/> | <span data-ttu-id="82797-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="82797-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="82797-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82797-128">Minimum supported server</span></span><br/> | <span data-ttu-id="82797-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="82797-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="82797-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82797-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="82797-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="82797-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="82797-132">IDL</span><span class="sxs-lookup"><span data-stu-id="82797-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82797-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82797-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82797-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="82797-134">See also</span></span>

<dl> <span data-ttu-id="82797-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="82797-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="82797-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="82797-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





