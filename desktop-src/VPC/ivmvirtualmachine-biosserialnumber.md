---
title: Propiedad IVMVirtualMachine BIOSSerialNumber (VPCCOMInterfaces. h)
description: Número de serie del BIOS.
ms.assetid: a105009d-1c44-4079-a7d4-103cb02bad71
keywords:
- Propiedad BIOSSerialNumber Virtual PC
- Propiedad BIOSSerialNumber Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad BIOSSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSSerialNumber
- IVMVirtualMachine.get_BIOSSerialNumber
- IVMVirtualMachine.put_BIOSSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8bd3f240d863a6f43dabbdb0a26429c4a77219
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079674"
---
# <a name="ivmvirtualmachinebiosserialnumber-property"></a><span data-ttu-id="27da9-106">IVMVirtualMachine:: BIOSSerialNumber (propiedad)</span><span class="sxs-lookup"><span data-stu-id="27da9-106">IVMVirtualMachine::BIOSSerialNumber property</span></span>

<span data-ttu-id="27da9-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="27da9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="27da9-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="27da9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="27da9-109">Recupera y establece el número de serie del BIOS.</span><span class="sxs-lookup"><span data-stu-id="27da9-109">Retrieves and sets the BIOS serial number.</span></span>

<span data-ttu-id="27da9-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="27da9-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="27da9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27da9-111">Syntax</span></span>


```C++
HRESULT put_BIOSSerialNumber(
  [in]          BSTR biosSerialNumber
);

HRESULT get_BIOSSerialNumber(
  [out, retval] BSTR *biosSerialNumber
);
```



## <a name="property-value"></a><span data-ttu-id="27da9-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="27da9-112">Property value</span></span>

<span data-ttu-id="27da9-113">Especifica el número de serie del BIOS.</span><span class="sxs-lookup"><span data-stu-id="27da9-113">Specifies the BIOS serial number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27da9-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="27da9-114">Error codes</span></span>



| <span data-ttu-id="27da9-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="27da9-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="27da9-116">Significado</span><span class="sxs-lookup"><span data-stu-id="27da9-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27da9-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="27da9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="27da9-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="27da9-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="27da9-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="27da9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="27da9-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="27da9-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="27da9-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="27da9-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="27da9-122">El parámetro tiene más de 32 caracteres, una cadena vacía o no es válido.</span><span class="sxs-lookup"><span data-stu-id="27da9-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="27da9-123"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="27da9-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="27da9-124">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="27da9-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="27da9-125"><dt>Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="27da9-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="27da9-126">La máquina virtual está en estado en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="27da9-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="27da9-127"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="27da9-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="27da9-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="27da9-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="27da9-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27da9-129">Remarks</span></span>

<span data-ttu-id="27da9-130">Esta propiedad no contendrá información válida hasta que la máquina virtual se haya iniciado por primera vez.</span><span class="sxs-lookup"><span data-stu-id="27da9-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="27da9-131">Se devolverá una cadena vacía si se lee antes del inicio inicial.</span><span class="sxs-lookup"><span data-stu-id="27da9-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="27da9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27da9-132">Requirements</span></span>



| <span data-ttu-id="27da9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="27da9-133">Requirement</span></span> | <span data-ttu-id="27da9-134">Value</span><span class="sxs-lookup"><span data-stu-id="27da9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27da9-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27da9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="27da9-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="27da9-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27da9-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27da9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="27da9-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="27da9-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="27da9-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="27da9-139">End of client support</span></span><br/>    | <span data-ttu-id="27da9-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27da9-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="27da9-141">Producto</span><span class="sxs-lookup"><span data-stu-id="27da9-141">Product</span></span><br/>                  | <span data-ttu-id="27da9-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="27da9-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="27da9-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27da9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="27da9-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="27da9-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="27da9-145">IID</span><span class="sxs-lookup"><span data-stu-id="27da9-145">IID</span></span><br/>                      | <span data-ttu-id="27da9-146">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="27da9-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="27da9-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="27da9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27da9-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="27da9-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

