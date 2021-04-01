---
title: Método _ID IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Recupera el identificador interno de esta interfaz de red.
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- _ID método virtual PC
- Método _ID Virtual PC, interfaz IVMNetworkAdapter
- Interfaz IVMNetworkAdapter Virtual PC, método _ID
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9df514d24f9826b58964b4c51c9a76a9ba982e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996517"
---
# <a name="ivmnetworkadapter_id-method"></a><span data-ttu-id="2e889-106">IVMNetworkAdapter:: \_ ID (método)</span><span class="sxs-lookup"><span data-stu-id="2e889-106">IVMNetworkAdapter::\_ID method</span></span>

<span data-ttu-id="2e889-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2e889-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2e889-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2e889-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2e889-109">Recupera el identificador interno de esta interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="2e889-109">Retrieves the internal identifier of this network interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e889-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e889-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a><span data-ttu-id="2e889-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e889-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e889-112">*identificador de* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e889-112">*identifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e889-113">Identificador interno.</span><span class="sxs-lookup"><span data-stu-id="2e889-113">The internal identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e889-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e889-114">Return value</span></span>

<span data-ttu-id="2e889-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2e889-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2e889-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e889-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="2e889-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e889-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2e889-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2e889-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2e889-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e889-119">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="2e889-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2e889-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2e889-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="2e889-121">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="2e889-122"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2e889-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="2e889-123">No se encuentra la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2e889-123">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="2e889-124"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2e889-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2e889-125">La operación tuvo un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="2e889-125">The operation had an unknown error.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="2e889-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e889-126">Remarks</span></span>

<span data-ttu-id="2e889-127">Este método no se puede usar en los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="2e889-127">This method is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e889-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e889-128">Requirements</span></span>



| <span data-ttu-id="2e889-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e889-129">Requirement</span></span> | <span data-ttu-id="2e889-130">Value</span><span class="sxs-lookup"><span data-stu-id="2e889-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e889-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e889-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2e889-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e889-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e889-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e889-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2e889-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2e889-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2e889-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2e889-135">End of client support</span></span><br/>    | <span data-ttu-id="2e889-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2e889-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2e889-137">Producto</span><span class="sxs-lookup"><span data-stu-id="2e889-137">Product</span></span><br/>                  | <span data-ttu-id="2e889-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2e889-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2e889-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e889-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e889-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e889-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2e889-141">IID</span><span class="sxs-lookup"><span data-stu-id="2e889-141">IID</span></span><br/>                      | <span data-ttu-id="2e889-142">IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="2e889-142">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2e889-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e889-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e889-144">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="2e889-144">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

