---
title: Propiedad IVMHostInfo OSMajorVersion (VPCCOMInterfaces. h)
description: Recupera la versión principal del sistema operativo que se ejecuta en el equipo host.
ms.assetid: d0b62d2d-532f-45c7-8622-67176b9b4a8f
keywords:
- Propiedad OSMajorVersion Virtual PC
- Propiedad OSMajorVersion Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad OSMajorVersion
topic_type:
- apiref
api_name:
- IVMHostInfo.OSMajorVersion
- IVMHostInfo.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf064744d90ede010a7e48e0e23e6a62a19eb4af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421891"
---
# <a name="ivmhostinfoosmajorversion-property"></a><span data-ttu-id="5795f-106">IVMHostInfo:: OSMajorVersion (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5795f-106">IVMHostInfo::OSMajorVersion property</span></span>

<span data-ttu-id="5795f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5795f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5795f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5795f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5795f-109">Recupera la versión principal del sistema operativo que se ejecuta en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="5795f-109">Retrieves the major version of the operating system running on the host machine.</span></span>

<span data-ttu-id="5795f-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5795f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5795f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5795f-111">Syntax</span></span>


```C++
HRESULT get_OSMajorVersion(
  [out, retval] long *osMajorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="5795f-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5795f-112">Property value</span></span>

<span data-ttu-id="5795f-113">Versión principal.</span><span class="sxs-lookup"><span data-stu-id="5795f-113">The major version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5795f-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5795f-114">Error codes</span></span>



| <span data-ttu-id="5795f-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="5795f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="5795f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5795f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5795f-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5795f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5795f-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5795f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="5795f-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5795f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="5795f-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="5795f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="5795f-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5795f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5795f-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="5795f-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5795f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5795f-123">Requirements</span></span>



| <span data-ttu-id="5795f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5795f-124">Requirement</span></span> | <span data-ttu-id="5795f-125">Value</span><span class="sxs-lookup"><span data-stu-id="5795f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5795f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5795f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5795f-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5795f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5795f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5795f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5795f-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5795f-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5795f-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5795f-130">End of client support</span></span><br/>    | <span data-ttu-id="5795f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5795f-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5795f-132">Producto</span><span class="sxs-lookup"><span data-stu-id="5795f-132">Product</span></span><br/>                  | <span data-ttu-id="5795f-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5795f-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5795f-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5795f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5795f-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5795f-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5795f-136">IID</span><span class="sxs-lookup"><span data-stu-id="5795f-136">IID</span></span><br/>                      | <span data-ttu-id="5795f-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="5795f-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="5795f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5795f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5795f-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="5795f-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

