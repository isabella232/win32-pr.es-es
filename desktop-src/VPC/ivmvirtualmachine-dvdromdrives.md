---
title: Propiedad IVMVirtualMachine DVDROMDrives (VPCCOMInterfaces. h)
description: Recupera una colección enumerable de unidades de CD y DVD conectadas a la máquina virtual.
ms.assetid: e9e7d912-568f-4a3d-85cf-63f6fa99cb19
keywords:
- Propiedad DVDROMDrives Virtual PC
- Propiedad DVDROMDrives Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad DVDROMDrives
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DVDROMDrives
- IVMVirtualMachine.get_DVDROMDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9980d783b19bfef7ce5437253b7923d6e6a2ebf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535175"
---
# <a name="ivmvirtualmachinedvdromdrives-property"></a><span data-ttu-id="c8c95-106">IVMVirtualMachine::D propiedad VDROMDrives</span><span class="sxs-lookup"><span data-stu-id="c8c95-106">IVMVirtualMachine::DVDROMDrives property</span></span>

<span data-ttu-id="c8c95-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c8c95-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8c95-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8c95-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8c95-109">Recupera una colección enumerable de unidades de CD y DVD conectadas a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8c95-109">Retrieves an enumerable collection of CD and DVD drives attached to the virtual machine.</span></span>

<span data-ttu-id="c8c95-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c8c95-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c95-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8c95-111">Syntax</span></span>


```C++
HRESULT get_DVDROMDrives(
  [out, retval] IVMDVDDriveCollection **dvdROMCollection
);
```



## <a name="property-value"></a><span data-ttu-id="c8c95-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c8c95-112">Property value</span></span>

<span data-ttu-id="c8c95-113">Objeto [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c8c95-113">An [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8c95-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c8c95-114">Error codes</span></span>



| <span data-ttu-id="c8c95-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="c8c95-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c8c95-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c8c95-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c8c95-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8c95-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c8c95-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8c95-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c8c95-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c8c95-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c8c95-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="c8c95-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c8c95-121"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c8c95-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c8c95-122">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="c8c95-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="c8c95-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c8c95-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c8c95-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="c8c95-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c8c95-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8c95-125">Requirements</span></span>



| <span data-ttu-id="c8c95-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8c95-126">Requirement</span></span> | <span data-ttu-id="c8c95-127">Value</span><span class="sxs-lookup"><span data-stu-id="c8c95-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c95-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c95-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c95-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8c95-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8c95-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c95-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8c95-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c8c95-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c8c95-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c8c95-132">End of client support</span></span><br/>    | <span data-ttu-id="c8c95-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8c95-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c8c95-134">Producto</span><span class="sxs-lookup"><span data-stu-id="c8c95-134">Product</span></span><br/>                  | <span data-ttu-id="c8c95-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8c95-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c8c95-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8c95-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8c95-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8c95-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c8c95-138">IID</span><span class="sxs-lookup"><span data-stu-id="c8c95-138">IID</span></span><br/>                      | <span data-ttu-id="c8c95-139">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c8c95-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c8c95-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8c95-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8c95-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="c8c95-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

