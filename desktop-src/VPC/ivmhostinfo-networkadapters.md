---
title: Propiedad IVMHostInfo adaptadores (VPCCOMInterfaces. h)
description: Recupera una colección enumerable de NIC en el equipo host.
ms.assetid: 17393d7a-c883-4d67-826b-83b886c0d7a6
keywords:
- Propiedad adaptadores Virtual PC
- Propiedad adaptadores Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad adaptadores
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAdapters
- IVMHostInfo.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeff5c6d459fb8f6999f896c3c13fcd980bf70ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995897"
---
# <a name="ivmhostinfonetworkadapters-property"></a><span data-ttu-id="5ea07-106">IVMHostInfo:: adaptadores (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5ea07-106">IVMHostInfo::NetworkAdapters property</span></span>

<span data-ttu-id="5ea07-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5ea07-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5ea07-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5ea07-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5ea07-109">Recupera una colección enumerable de NIC en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="5ea07-109">Retrieves an enumerable collection of NICs in the host machine.</span></span>

<span data-ttu-id="5ea07-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5ea07-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea07-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ea07-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] VARIANT *hostNICs
);
```



## <a name="property-value"></a><span data-ttu-id="5ea07-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5ea07-112">Property value</span></span>

<span data-ttu-id="5ea07-113">Colección de tarjetas de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="5ea07-113">A collection of network interface cards.</span></span> <span data-ttu-id="5ea07-114">Se trata de una matriz de valores **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="5ea07-114">This is an array of **BSTR** values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5ea07-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5ea07-115">Error codes</span></span>



| <span data-ttu-id="5ea07-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="5ea07-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="5ea07-117">Significado</span><span class="sxs-lookup"><span data-stu-id="5ea07-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5ea07-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5ea07-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5ea07-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5ea07-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="5ea07-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5ea07-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="5ea07-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="5ea07-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="5ea07-122"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5ea07-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5ea07-123">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="5ea07-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5ea07-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ea07-124">Requirements</span></span>



| <span data-ttu-id="5ea07-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ea07-125">Requirement</span></span> | <span data-ttu-id="5ea07-126">Value</span><span class="sxs-lookup"><span data-stu-id="5ea07-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea07-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ea07-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea07-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ea07-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ea07-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ea07-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea07-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5ea07-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5ea07-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5ea07-131">End of client support</span></span><br/>    | <span data-ttu-id="5ea07-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ea07-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5ea07-133">Producto</span><span class="sxs-lookup"><span data-stu-id="5ea07-133">Product</span></span><br/>                  | <span data-ttu-id="5ea07-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5ea07-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5ea07-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ea07-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ea07-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ea07-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5ea07-137">IID</span><span class="sxs-lookup"><span data-stu-id="5ea07-137">IID</span></span><br/>                      | <span data-ttu-id="5ea07-138">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="5ea07-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="5ea07-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ea07-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea07-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="5ea07-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

