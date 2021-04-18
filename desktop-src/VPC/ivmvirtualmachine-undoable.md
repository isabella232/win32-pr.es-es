---
title: Propiedad IVMVirtualMachine deshacer (VPCCOMInterfaces. h)
description: Determina si las unidades de deshacer están habilitadas para los discos duros conectados a la máquina virtual.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- PC virtual de propiedades que se puedan deshacer
- Propiedad deshacer de Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad deshacer
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cbc77f4d68fbdbfcc8d3998e3c207b8f4245c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534240"
---
# <a name="ivmvirtualmachineundoable-property"></a><span data-ttu-id="338cd-106">Propiedad IVMVirtualMachine:: Undoable</span><span class="sxs-lookup"><span data-stu-id="338cd-106">IVMVirtualMachine::Undoable property</span></span>

<span data-ttu-id="338cd-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="338cd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="338cd-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="338cd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="338cd-109">Determina si las unidades de deshacer están habilitadas para los discos duros conectados a la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="338cd-109">Determines whether undo drives are enabled for hard disks connected to the virtual machine (VM).</span></span>

<span data-ttu-id="338cd-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="338cd-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="338cd-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="338cd-111">Syntax</span></span>


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a><span data-ttu-id="338cd-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="338cd-112">Property value</span></span>

<span data-ttu-id="338cd-113">Especifica **Variant \_ true** si las unidades de deshacer están habilitadas para los discos duros conectados a la máquina virtual y **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="338cd-113">Specifies **VARIANT\_TRUE** if undo drives are enabled for hard disks connected to the VM and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="338cd-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="338cd-114">Error codes</span></span>



| <span data-ttu-id="338cd-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="338cd-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="338cd-116">Significado</span><span class="sxs-lookup"><span data-stu-id="338cd-116">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="338cd-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="338cd-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="338cd-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="338cd-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="338cd-119"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="338cd-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="338cd-120">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="338cd-120">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="338cd-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="338cd-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="338cd-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="338cd-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="338cd-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="338cd-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="338cd-124">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="338cd-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="338cd-125"><dt>Máquina virtual \_ E \_ preft \_ VM \_ Active</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="338cd-125"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="338cd-126">La máquina virtual se está ejecutando o guardando.</span><span class="sxs-lookup"><span data-stu-id="338cd-126">The VM is running or saved.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="338cd-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="338cd-127">Remarks</span></span>

<span data-ttu-id="338cd-128">Si se deshabilitan las unidades de deshacer, se eliminarán los archivos de las unidades de deshacer existentes.</span><span class="sxs-lookup"><span data-stu-id="338cd-128">If undo drives are disabled, any existing undo drive files will be deleted.</span></span>

<span data-ttu-id="338cd-129">No se puede establecer esta propiedad si la máquina virtual está en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="338cd-129">You cannot set this property if the VM is running or saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="338cd-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="338cd-130">Requirements</span></span>



| <span data-ttu-id="338cd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="338cd-131">Requirement</span></span> | <span data-ttu-id="338cd-132">Value</span><span class="sxs-lookup"><span data-stu-id="338cd-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="338cd-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="338cd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="338cd-134">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="338cd-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="338cd-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="338cd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="338cd-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="338cd-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="338cd-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="338cd-137">End of client support</span></span><br/>    | <span data-ttu-id="338cd-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="338cd-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="338cd-139">Producto</span><span class="sxs-lookup"><span data-stu-id="338cd-139">Product</span></span><br/>                  | <span data-ttu-id="338cd-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="338cd-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="338cd-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="338cd-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="338cd-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="338cd-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="338cd-143">IID</span><span class="sxs-lookup"><span data-stu-id="338cd-143">IID</span></span><br/>                      | <span data-ttu-id="338cd-144">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="338cd-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="338cd-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="338cd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338cd-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="338cd-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

