---
title: Propiedad IVMHostInfo SerialPorts (VPCCOMInterfaces. h)
description: Recupera los nombres de puerto serie asociados a los puertos serie del host.
ms.assetid: ef3bc474-19c9-4d91-8aa0-7619c89fec2d
keywords:
- Propiedad SerialPorts Virtual PC
- Propiedad SerialPorts Virtual PC, interfaz IVMHostInfo
- Interfaz IVMHostInfo Virtual PC, propiedad SerialPorts
topic_type:
- apiref
api_name:
- IVMHostInfo.SerialPorts
- IVMHostInfo.get_SerialPorts
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8cb520ee82b53e93f9073b66d4dc4d69a2ef75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078813"
---
# <a name="ivmhostinfoserialports-property"></a><span data-ttu-id="02c59-106">IVMHostInfo:: SerialPorts (propiedad)</span><span class="sxs-lookup"><span data-stu-id="02c59-106">IVMHostInfo::SerialPorts property</span></span>

<span data-ttu-id="02c59-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02c59-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="02c59-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="02c59-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="02c59-109">Recupera los nombres de puerto serie asociados a los puertos serie del host.</span><span class="sxs-lookup"><span data-stu-id="02c59-109">Retrieves the serial port names associated with host serial ports.</span></span>

<span data-ttu-id="02c59-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="02c59-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c59-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02c59-111">Syntax</span></span>


```C++
HRESULT get_SerialPorts(
  [out, retval] BSTR *serialPorts
);
```



## <a name="property-value"></a><span data-ttu-id="02c59-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="02c59-112">Property value</span></span>

<span data-ttu-id="02c59-113">Una lista delimitada por signos de punto y coma de nombres de puertos serie.</span><span class="sxs-lookup"><span data-stu-id="02c59-113">A semicolon-delimited list of serial port names.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02c59-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="02c59-114">Error codes</span></span>



| <span data-ttu-id="02c59-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="02c59-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="02c59-116">Significado</span><span class="sxs-lookup"><span data-stu-id="02c59-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="02c59-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="02c59-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="02c59-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="02c59-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="02c59-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="02c59-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="02c59-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="02c59-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="02c59-121"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="02c59-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="02c59-122">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="02c59-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="02c59-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02c59-123">Requirements</span></span>



| <span data-ttu-id="02c59-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c59-124">Requirement</span></span> | <span data-ttu-id="02c59-125">Value</span><span class="sxs-lookup"><span data-stu-id="02c59-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c59-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02c59-126">Minimum supported client</span></span><br/> | <span data-ttu-id="02c59-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="02c59-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02c59-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02c59-128">Minimum supported server</span></span><br/> | <span data-ttu-id="02c59-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="02c59-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="02c59-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="02c59-130">End of client support</span></span><br/>    | <span data-ttu-id="02c59-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02c59-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="02c59-132">Producto</span><span class="sxs-lookup"><span data-stu-id="02c59-132">Product</span></span><br/>                  | <span data-ttu-id="02c59-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="02c59-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="02c59-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02c59-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="02c59-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="02c59-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="02c59-136">IID</span><span class="sxs-lookup"><span data-stu-id="02c59-136">IID</span></span><br/>                      | <span data-ttu-id="02c59-137">IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="02c59-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="02c59-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="02c59-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c59-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="02c59-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

