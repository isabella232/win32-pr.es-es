---
title: Método INapComponentInfo GetVendorName (NapCommon. h)
description: Lo usa el sistema NAP para obtener el nombre del proveedor de un cliente de mantenimiento.
ms.assetid: 7083b0b6-38fc-4c24-a5f7-fe0a1ebd5e88
keywords:
- Método GetVendorName NAP
- Método GetVendorName NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetVendorName
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVendorName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3c82f4e7e4f76d827e71421c467a8a223428a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493252"
---
# <a name="inapcomponentinfogetvendorname-method"></a><span data-ttu-id="a535d-106">INapComponentInfo:: GetVendorName (método)</span><span class="sxs-lookup"><span data-stu-id="a535d-106">INapComponentInfo::GetVendorName method</span></span>

> [!Note]  
> <span data-ttu-id="a535d-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a535d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a535d-108">El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: GetVendorName** para obtener el nombre del proveedor de un cliente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="a535d-108">The **INapComponentInfo::GetVendorName** callback method is used by the NAP System to get the vendor name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a535d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a535d-109">Syntax</span></span>


```C++
HRESULT GetVendorName(
  [out] MessageId *vendorName
);
```



## <a name="parameters"></a><span data-ttu-id="a535d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a535d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a535d-111">*Nombredelproveedor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a535d-111">*vendorName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a535d-112">Un puntero a un [**MessageId**](nap-datatypes.md) que contiene el identificador de recurso del nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a535d-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the vendor name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a535d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a535d-113">Return value</span></span>

<span data-ttu-id="a535d-114">Devuelva uno de estos códigos de error en función del resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="a535d-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="a535d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a535d-115">Return code</span></span>                                                                                     | <span data-ttu-id="a535d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a535d-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a535d-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="a535d-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a535d-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a535d-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="a535d-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a535d-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a535d-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="a535d-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a535d-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a535d-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a535d-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a535d-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a535d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a535d-123">Requirements</span></span>



| <span data-ttu-id="a535d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a535d-124">Requirement</span></span> | <span data-ttu-id="a535d-125">Value</span><span class="sxs-lookup"><span data-stu-id="a535d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a535d-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a535d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a535d-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a535d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a535d-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a535d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a535d-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a535d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a535d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a535d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a535d-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a535d-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="a535d-132">IDL</span><span class="sxs-lookup"><span data-stu-id="a535d-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a535d-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a535d-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a535d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a535d-134">See also</span></span>

<dl> <span data-ttu-id="a535d-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="a535d-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="a535d-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="a535d-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





