---
title: Propiedad IVMVirtualMachine Notes (VPCCOMInterfaces. h)
description: Notas para la máquina virtual.
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Propiedades de Notes Virtual PC
- Propiedad notas Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad notas
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8fba8659a8f9546866129f21299e44006eb496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492574"
---
# <a name="ivmvirtualmachinenotes-property"></a><span data-ttu-id="837ee-106">IVMVirtualMachine:: Notes (propiedad)</span><span class="sxs-lookup"><span data-stu-id="837ee-106">IVMVirtualMachine::Notes property</span></span>

<span data-ttu-id="837ee-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="837ee-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="837ee-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="837ee-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="837ee-109">Recupera y establece las notas de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="837ee-109">Retrieves and sets the notes for the virtual machine.</span></span>

<span data-ttu-id="837ee-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="837ee-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="837ee-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="837ee-111">Syntax</span></span>


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a><span data-ttu-id="837ee-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="837ee-112">Property value</span></span>

<span data-ttu-id="837ee-113">Especifica las notas de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="837ee-113">Specifies the notes for the virtual machine.</span></span> <span data-ttu-id="837ee-114">La longitud máxima de la cadena es de 65.536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="837ee-114">The maximum length of the string is 65,536 characters.</span></span>

<span data-ttu-id="837ee-115">Para quitar cualquier nota, pase una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="837ee-115">To remove any notes, pass an empty string.</span></span>

## <a name="error-codes"></a><span data-ttu-id="837ee-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="837ee-116">Error codes</span></span>



| <span data-ttu-id="837ee-117">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="837ee-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="837ee-118">Significado</span><span class="sxs-lookup"><span data-stu-id="837ee-118">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="837ee-119"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="837ee-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="837ee-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="837ee-120">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="837ee-121"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="837ee-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="837ee-122">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="837ee-122">The parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="837ee-123"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="837ee-123"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="837ee-124">El parámetro no es válido o contiene más de 65.536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="837ee-124">The parameter is not valid or contains more than 65,536 characters.</span></span><br/> |
| <dl> <span data-ttu-id="837ee-125"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="837ee-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="837ee-126">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="837ee-126">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="837ee-127"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="837ee-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="837ee-128">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="837ee-128">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="837ee-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="837ee-129">Requirements</span></span>



| <span data-ttu-id="837ee-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="837ee-130">Requirement</span></span> | <span data-ttu-id="837ee-131">Value</span><span class="sxs-lookup"><span data-stu-id="837ee-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="837ee-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="837ee-132">Minimum supported client</span></span><br/> | <span data-ttu-id="837ee-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="837ee-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="837ee-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="837ee-134">Minimum supported server</span></span><br/> | <span data-ttu-id="837ee-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="837ee-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="837ee-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="837ee-136">End of client support</span></span><br/>    | <span data-ttu-id="837ee-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="837ee-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="837ee-138">Producto</span><span class="sxs-lookup"><span data-stu-id="837ee-138">Product</span></span><br/>                  | <span data-ttu-id="837ee-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="837ee-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="837ee-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="837ee-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="837ee-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="837ee-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="837ee-142">IID</span><span class="sxs-lookup"><span data-stu-id="837ee-142">IID</span></span><br/>                      | <span data-ttu-id="837ee-143">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="837ee-143">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="837ee-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="837ee-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="837ee-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="837ee-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

