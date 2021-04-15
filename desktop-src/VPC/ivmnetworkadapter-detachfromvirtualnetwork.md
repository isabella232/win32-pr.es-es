---
title: Método IVMNetworkAdapter DetachFromVirtualNetwork (VPCCOMInterfaces. h)
description: Desasocia la interfaz de red de su red virtual.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- Método DetachFromVirtualNetwork Virtual PC
- Método DetachFromVirtualNetwork Virtual PC, interfaz IVMNetworkAdapter
- Interfaz IVMNetworkAdapter Virtual PC, método DetachFromVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d5046844764fe9e9eb6552fe1a04b6140201b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422386"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a><span data-ttu-id="92474-106">IVMNetworkAdapter::D método etachFromVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="92474-106">IVMNetworkAdapter::DetachFromVirtualNetwork method</span></span>

<span data-ttu-id="92474-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="92474-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="92474-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="92474-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="92474-109">Desasocia la interfaz de red de su red virtual.</span><span class="sxs-lookup"><span data-stu-id="92474-109">Detaches the network interface from its virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="92474-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92474-110">Syntax</span></span>


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a><span data-ttu-id="92474-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92474-111">Parameters</span></span>

<span data-ttu-id="92474-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="92474-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92474-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92474-113">Return value</span></span>

<span data-ttu-id="92474-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="92474-114">This method can return one of these values.</span></span>



| <span data-ttu-id="92474-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92474-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="92474-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="92474-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="92474-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="92474-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="92474-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="92474-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="92474-119"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="92474-119"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="92474-120">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="92474-120">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="92474-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92474-121">Requirements</span></span>



| <span data-ttu-id="92474-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="92474-122">Requirement</span></span> | <span data-ttu-id="92474-123">Value</span><span class="sxs-lookup"><span data-stu-id="92474-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="92474-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92474-124">Minimum supported client</span></span><br/> | <span data-ttu-id="92474-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="92474-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="92474-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92474-126">Minimum supported server</span></span><br/> | <span data-ttu-id="92474-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="92474-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="92474-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="92474-128">End of client support</span></span><br/>    | <span data-ttu-id="92474-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="92474-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="92474-130">Producto</span><span class="sxs-lookup"><span data-stu-id="92474-130">Product</span></span><br/>                  | <span data-ttu-id="92474-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="92474-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="92474-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92474-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="92474-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="92474-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="92474-134">IID</span><span class="sxs-lookup"><span data-stu-id="92474-134">IID</span></span><br/>                      | <span data-ttu-id="92474-135">IID \_ IVMNetworkAdapter se define como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="92474-135">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="92474-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="92474-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92474-137">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="92474-137">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

