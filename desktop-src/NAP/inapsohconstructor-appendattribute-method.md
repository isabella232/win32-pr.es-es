---
title: Método INapSoHConstructor AppendAttribute (NapProtocol. h)
description: Agrega un TLV al final del búfer de SoH.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Método AppendAttribute NAP
- Método AppendAttribute NAP, interfaz INapSoHConstructor
- Interfaz INapSoHConstructor NAP, método AppendAttribute
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534095"
---
# <a name="inapsohconstructorappendattribute-method"></a><span data-ttu-id="efd1e-106">INapSoHConstructor:: AppendAttribute (método)</span><span class="sxs-lookup"><span data-stu-id="efd1e-106">INapSoHConstructor::AppendAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="efd1e-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="efd1e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="efd1e-108">El método **INapSoHConstructor:: AppendAttribute** agrega un TLV al final del búfer de SOH.</span><span class="sxs-lookup"><span data-stu-id="efd1e-108">The **INapSoHConstructor::AppendAttribute** method adds a TLV to the end of the SoH buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="efd1e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efd1e-109">Syntax</span></span>


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="efd1e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efd1e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efd1e-111">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="efd1e-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efd1e-112">Una enumeración [**SoHAttributeType**](sohattributetype-enum.md) que indica el tipo de atributo del nuevo TLV.</span><span class="sxs-lookup"><span data-stu-id="efd1e-112">A [**SoHAttributeType**](sohattributetype-enum.md) enumeration that indicates the attribute type of the new TLV.</span></span>

</dd> <dt>

<span data-ttu-id="efd1e-113">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="efd1e-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efd1e-114">Puntero a una estructura [**SoHAttributeValue**](sohattributevalue-union.md) que contiene el valor para el nuevo TLV.</span><span class="sxs-lookup"><span data-stu-id="efd1e-114">A pointer to an [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the value for the new TLV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efd1e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efd1e-115">Return value</span></span>

<span data-ttu-id="efd1e-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="efd1e-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="efd1e-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="efd1e-117">Return code</span></span>                                                                                     | <span data-ttu-id="efd1e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="efd1e-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="efd1e-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="efd1e-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="efd1e-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="efd1e-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="efd1e-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="efd1e-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="efd1e-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="efd1e-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="efd1e-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="efd1e-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="efd1e-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="efd1e-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efd1e-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efd1e-125">Remarks</span></span>

<span data-ttu-id="efd1e-126">El TLV [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) no debe agregarse mediante esta función.</span><span class="sxs-lookup"><span data-stu-id="efd1e-126">The [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV must not be added using this function.</span></span> <span data-ttu-id="efd1e-127">Se agrega como primer TLV de [**INapSoHConstructor:: Initialize**](inapsohconstructor-initialize-method.md) a paquetes SOH recién construidos.</span><span class="sxs-lookup"><span data-stu-id="efd1e-127">It is added as the first TLV by [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) to newly constructed SOH packets.</span></span>

<span data-ttu-id="efd1e-128">Al anexar un atributo que utilizará el sistema NAP, no debe cifrarse ni modificarse de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="efd1e-128">When appending an attribute which will be consumed by the Nap System, it should not be encrypted or modified in any manner.</span></span> <span data-ttu-id="efd1e-129">Si el HealthEntity requiere la comprobación de la integridad y el cifrado (MACs) de la información privada, solo debe incluirse en el atributo [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) .</span><span class="sxs-lookup"><span data-stu-id="efd1e-129">If the HealthEntity requires encryption/integrity checking (MACs) of private information, it should be included only in the [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="efd1e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efd1e-130">Requirements</span></span>



| <span data-ttu-id="efd1e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="efd1e-131">Requirement</span></span> | <span data-ttu-id="efd1e-132">Value</span><span class="sxs-lookup"><span data-stu-id="efd1e-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="efd1e-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efd1e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="efd1e-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="efd1e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="efd1e-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efd1e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="efd1e-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="efd1e-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="efd1e-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efd1e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="efd1e-138"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="efd1e-138"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="efd1e-139">IDL</span><span class="sxs-lookup"><span data-stu-id="efd1e-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="efd1e-140"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="efd1e-140"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="efd1e-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="efd1e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efd1e-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efd1e-142"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="efd1e-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="efd1e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd1e-144">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="efd1e-144">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





