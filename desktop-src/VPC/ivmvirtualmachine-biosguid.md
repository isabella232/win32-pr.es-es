---
title: Propiedad IVMVirtualMachine BIOSGUID (VPCCOMInterfaces. h)
description: GUID del BIOS.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- Propiedad BIOSGUID Virtual PC
- Propiedad BIOSGUID Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad BIOSGUID
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905213"
---
# <a name="ivmvirtualmachinebiosguid-property"></a><span data-ttu-id="e2946-106">IVMVirtualMachine:: BIOSGUID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e2946-106">IVMVirtualMachine::BIOSGUID property</span></span>

<span data-ttu-id="e2946-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e2946-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e2946-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e2946-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e2946-109">Recupera y establece el GUID del BIOS.</span><span class="sxs-lookup"><span data-stu-id="e2946-109">Retrieves and sets the BIOS GUID.</span></span>

<span data-ttu-id="e2946-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e2946-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2946-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2946-111">Syntax</span></span>


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a><span data-ttu-id="e2946-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e2946-112">Property value</span></span>

<span data-ttu-id="e2946-113">Especifica el GUID del BIOS.</span><span class="sxs-lookup"><span data-stu-id="e2946-113">Specifies the BIOS GUID.</span></span> <span data-ttu-id="e2946-114">Incluya las llaves izquierda y derecha en torno a los dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="e2946-114">Include left and right braces around the hex digits.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e2946-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e2946-115">Error codes</span></span>



| <span data-ttu-id="e2946-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="e2946-116">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="e2946-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e2946-117">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="e2946-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2946-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="e2946-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e2946-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="e2946-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e2946-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="e2946-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="e2946-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="e2946-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e2946-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="e2946-123">El parámetro no es válido o es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="e2946-123">The parameter is not valid or is an empty string.</span></span><br/>   |
| <dl> <span data-ttu-id="e2946-124"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e2946-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="e2946-125">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="e2946-125">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="e2946-126"><dt>Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="e2946-126"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="e2946-127">La máquina virtual está en estado en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="e2946-127">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="e2946-128"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e2946-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="e2946-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="e2946-129">An unexpected error has occurred.</span></span><br/>                   |



## <a name="remarks"></a><span data-ttu-id="e2946-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2946-130">Remarks</span></span>

<span data-ttu-id="e2946-131">Esta propiedad no contendrá información válida hasta que la máquina virtual se haya iniciado por primera vez.</span><span class="sxs-lookup"><span data-stu-id="e2946-131">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="e2946-132">Se devolverá una cadena vacía si se lee antes del inicio inicial.</span><span class="sxs-lookup"><span data-stu-id="e2946-132">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2946-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2946-133">Requirements</span></span>



| <span data-ttu-id="e2946-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2946-134">Requirement</span></span> | <span data-ttu-id="e2946-135">Value</span><span class="sxs-lookup"><span data-stu-id="e2946-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2946-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2946-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e2946-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2946-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2946-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2946-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e2946-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e2946-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e2946-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e2946-140">End of client support</span></span><br/>    | <span data-ttu-id="e2946-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2946-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e2946-142">Producto</span><span class="sxs-lookup"><span data-stu-id="e2946-142">Product</span></span><br/>                  | <span data-ttu-id="e2946-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e2946-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e2946-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2946-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2946-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2946-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e2946-146">IID</span><span class="sxs-lookup"><span data-stu-id="e2946-146">IID</span></span><br/>                      | <span data-ttu-id="e2946-147">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e2946-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e2946-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2946-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2946-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e2946-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

