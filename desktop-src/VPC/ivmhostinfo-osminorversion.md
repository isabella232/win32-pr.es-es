---
title: Propiedad IVMHostInfo OSMinorVersion (VPCCOMInterfaces. h)
description: Recupera la versión secundaria del sistema operativo que se ejecuta en el equipo host.
ms.assetid: 12f3ac59-ab7d-40f6-a0e6-fb870d2dff16
keywords:
- Propiedad OSMinorVersion Virtual PC
- Propiedad OSMinorVersion Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad OSMinorVersion
topic_type:
- apiref
api_name:
- IVMHostInfo.OSMinorVersion
- IVMHostInfo.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3063a752886ebd196f1462ce67572fe62d032f4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149860"
---
# <a name="ivmhostinfoosminorversion-property"></a><span data-ttu-id="a8b64-106">IVMHostInfo:: OSMinorVersion (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a8b64-106">IVMHostInfo::OSMinorVersion property</span></span>

<span data-ttu-id="a8b64-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a8b64-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a8b64-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a8b64-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a8b64-109">Recupera la versión secundaria del sistema operativo que se ejecuta en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="a8b64-109">Retrieves the minor version of the operating system running on the host machine.</span></span>

<span data-ttu-id="a8b64-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a8b64-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b64-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8b64-111">Syntax</span></span>


```C++
HRESULT get_OSMinorVersion(
  [out, retval] long *osMinorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="a8b64-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a8b64-112">Property value</span></span>

<span data-ttu-id="a8b64-113">Versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="a8b64-113">The minor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a8b64-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a8b64-114">Error codes</span></span>



| <span data-ttu-id="a8b64-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="a8b64-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a8b64-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a8b64-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a8b64-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a8b64-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a8b64-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8b64-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a8b64-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a8b64-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a8b64-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="a8b64-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a8b64-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a8b64-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a8b64-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a8b64-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a8b64-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8b64-123">Requirements</span></span>



| <span data-ttu-id="a8b64-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b64-124">Requirement</span></span> | <span data-ttu-id="a8b64-125">Value</span><span class="sxs-lookup"><span data-stu-id="a8b64-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b64-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8b64-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b64-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8b64-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8b64-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8b64-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b64-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a8b64-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a8b64-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a8b64-130">End of client support</span></span><br/>    | <span data-ttu-id="a8b64-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a8b64-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a8b64-132">Producto</span><span class="sxs-lookup"><span data-stu-id="a8b64-132">Product</span></span><br/>                  | <span data-ttu-id="a8b64-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a8b64-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a8b64-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8b64-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b64-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b64-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a8b64-136">IID</span><span class="sxs-lookup"><span data-stu-id="a8b64-136">IID</span></span><br/>                      | <span data-ttu-id="a8b64-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="a8b64-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a8b64-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8b64-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b64-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="a8b64-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

