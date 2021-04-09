---
title: Método _ID IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera el identificador interno de la red virtual.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- _ID método virtual PC
- Método _ID Virtual PC, interfaz IVMVirtualNetwork
- Interfaz IVMVirtualNetwork Virtual PC, método _ID
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079671"
---
# <a name="ivmvirtualnetwork_id-method"></a><span data-ttu-id="ca46f-106">IVMVirtualNetwork:: \_ ID (método)</span><span class="sxs-lookup"><span data-stu-id="ca46f-106">IVMVirtualNetwork::\_ID method</span></span>

<span data-ttu-id="ca46f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ca46f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ca46f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ca46f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ca46f-109">Recupera el identificador interno de la red virtual.</span><span class="sxs-lookup"><span data-stu-id="ca46f-109">Retrieves the internal identifier of the virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca46f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca46f-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a><span data-ttu-id="ca46f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca46f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca46f-112">*virtualNetworkID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ca46f-112">*virtualNetworkID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca46f-113">Identificador de red virtual.</span><span class="sxs-lookup"><span data-stu-id="ca46f-113">The virtual network identifier.</span></span> <span data-ttu-id="ca46f-114">El identificador de la red virtual de redes compartidas (NAT) es 01010101010101010101010101010101.</span><span class="sxs-lookup"><span data-stu-id="ca46f-114">The identifier for the Shared Networking (NAT) virtual network is 01010101010101010101010101010101.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca46f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca46f-115">Return value</span></span>

<span data-ttu-id="ca46f-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ca46f-116">This method can return one of these values.</span></span>



| <span data-ttu-id="ca46f-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca46f-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="ca46f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca46f-118">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ca46f-119"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ca46f-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ca46f-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ca46f-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ca46f-121"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ca46f-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ca46f-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="ca46f-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="ca46f-123"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ca46f-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ca46f-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="ca46f-124">An unexpected error has occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca46f-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca46f-125">Remarks</span></span>

<span data-ttu-id="ca46f-126">Esta propiedad no se puede usar en los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="ca46f-126">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca46f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca46f-127">Requirements</span></span>



| <span data-ttu-id="ca46f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca46f-128">Requirement</span></span> | <span data-ttu-id="ca46f-129">Value</span><span class="sxs-lookup"><span data-stu-id="ca46f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca46f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca46f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ca46f-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca46f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca46f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca46f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ca46f-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ca46f-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ca46f-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ca46f-134">End of client support</span></span><br/>    | <span data-ttu-id="ca46f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca46f-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ca46f-136">Producto</span><span class="sxs-lookup"><span data-stu-id="ca46f-136">Product</span></span><br/>                  | <span data-ttu-id="ca46f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ca46f-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ca46f-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca46f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca46f-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca46f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ca46f-140">IID</span><span class="sxs-lookup"><span data-stu-id="ca46f-140">IID</span></span><br/>                      | <span data-ttu-id="ca46f-141">IID \_ IVMVirtualNetwork se define como 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="ca46f-141">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ca46f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca46f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca46f-143">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="ca46f-143">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

