---
title: Propiedad nombre de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Nombre de la configuración de la máquina virtual.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Propiedad nombre virtual PC
- Propiedad nombre virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150426"
---
# <a name="ivmvirtualmachinename-property"></a><span data-ttu-id="91b39-106">IVMVirtualMachine:: Name (propiedad)</span><span class="sxs-lookup"><span data-stu-id="91b39-106">IVMVirtualMachine::Name property</span></span>

<span data-ttu-id="91b39-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="91b39-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="91b39-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="91b39-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="91b39-109">Recupera y establece el nombre de la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91b39-109">Retrieves and sets the name of the virtual machine configuration.</span></span>

<span data-ttu-id="91b39-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="91b39-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b39-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91b39-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a><span data-ttu-id="91b39-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="91b39-112">Property value</span></span>

<span data-ttu-id="91b39-113">Especifica el nombre de la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91b39-113">Specifies the name of the virtual machine configuration.</span></span> <span data-ttu-id="91b39-114">La longitud del nombre no puede superar los 80 caracteres y la longitud total de la ruta de acceso completa que incluye el archivo de configuración del nombre de la máquina virtual no puede superar los caracteres de la **\_ ruta de acceso máxima** (260).</span><span class="sxs-lookup"><span data-stu-id="91b39-114">The length of the name cannot be more than 80 characters and the total length of the fully qualified path that includes the virtual machine name configuration file cannot be more than **MAX\_PATH** (260) characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="91b39-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="91b39-115">Error codes</span></span>



| <span data-ttu-id="91b39-116">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="91b39-116">Name/value</span></span>                                                                                                                                                                    | <span data-ttu-id="91b39-117">Significado</span><span class="sxs-lookup"><span data-stu-id="91b39-117">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91b39-118"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91b39-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                       | <span data-ttu-id="91b39-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="91b39-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="91b39-120"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="91b39-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                         | <span data-ttu-id="91b39-121">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="91b39-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="91b39-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="91b39-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                      | <span data-ttu-id="91b39-123">El parámetro no es válido o es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="91b39-123">The parameter is not valid or is an empty string.</span></span><br/>                                    |
| <dl> <span data-ttu-id="91b39-124"><dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91b39-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                 | <span data-ttu-id="91b39-125">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="91b39-125">The configuration is unknown.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="91b39-126"><dt>Máquina virtual \_ E \_ preft \_ VM \_ Active</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="91b39-126"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl>            | <span data-ttu-id="91b39-127">La máquina virtual está en ejecución o guardada.</span><span class="sxs-lookup"><span data-stu-id="91b39-127">The virtual machine is running or saved.</span></span><br/>                                             |
| <dl> <span data-ttu-id="91b39-128"><dt>Máquina virtual \_ E \_ configuración \_ sin \_ nombre</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="91b39-128"><dt>VM\_E\_CONFIG\_NO\_NAME</dt> <dt>0xA0040400</dt></span></span> </dl>            | <span data-ttu-id="91b39-129">El parámetro *virtualMachineName* está vacío.</span><span class="sxs-lookup"><span data-stu-id="91b39-129">The *virtualMachineName* parameter is empty.</span></span><br/>                                         |
| <dl> <span data-ttu-id="91b39-130"><dt>Máquina virtual \_ E \_ nombre de configuración \_ \_ demasiado \_ largo</dt> <dt>0xA00400401</dt></span><span class="sxs-lookup"><span data-stu-id="91b39-130"><dt>VM\_E\_CONFIG\_NAME\_TOO\_LONG</dt> <dt>0xA00400401</dt></span></span> </dl>    | <span data-ttu-id="91b39-131">El parámetro contiene demasiados caracteres.</span><span class="sxs-lookup"><span data-stu-id="91b39-131">The parameter contains too many characters.</span></span><br/>                                          |
| <dl> <span data-ttu-id="91b39-132"><dt>Máquina virtual \_ E \_ nombre de configuración de 0xA0040402 \_ \_ \_ Char no válido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91b39-132"><dt>VM\_E\_CONFIG\_NAME\_INVALID\_CHAR</dt> <dt>0xA0040402</dt></span></span> </dl> | <span data-ttu-id="91b39-133">El parámetro contiene uno de los siguientes caracteres no válidos " \* ?: <>/ \| \\ " ".</span><span class="sxs-lookup"><span data-stu-id="91b39-133">The parameter contains one of the following invalid characters "\*?:<>/\|\\"".</span></span><br/> |
| <dl> <span data-ttu-id="91b39-134"><dt>Máquina virtual \_ E \_ configuración \_ \_ nombre duplicado</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="91b39-134"><dt>VM\_E\_CONFIG\_DUPLICATE\_NAME</dt> <dt>0xA0040403</dt></span></span> </dl>     | <span data-ttu-id="91b39-135">El nombre especificado ya existe como el nombre de otra máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91b39-135">The specified name already exists as the name of another virtual machine.</span></span><br/>            |
| <dl> <span data-ttu-id="91b39-136"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="91b39-136"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                 | <span data-ttu-id="91b39-137">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="91b39-137">An unexpected error has occurred.</span></span><br/>                                                    |



## <a name="remarks"></a><span data-ttu-id="91b39-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91b39-138">Remarks</span></span>

<span data-ttu-id="91b39-139">Los nombres de las máquinas virtuales no distinguen mayúsculas de minúsculas, por ejemplo, "MyVM" y "MyVM" hacen referencia a la misma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91b39-139">Virtual machine names are case-insensitive, e.g. "MyVM" and "myvm" refer to the same virtual machine.</span></span> <span data-ttu-id="91b39-140">Esta es la propiedad predeterminada para [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="91b39-140">This is the default property for [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="91b39-141">Si VPC.exe se está ejecutando y la máquina virtual se guarda, el establecimiento de la propiedad **Name** no se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="91b39-141">If VPC.exe is running and the VM is saved then setting the **Name** property will not succeed.</span></span> <span data-ttu-id="91b39-142">Si VPC.exe no se está ejecutando y se guarda la máquina virtual, el establecimiento de la propiedad **Name** se realizará correctamente cuando se inicie VPC.exe.</span><span class="sxs-lookup"><span data-stu-id="91b39-142">If VPC.exe is not running and the VM is saved then setting the **Name** property will succeed when VPC.exe is next started.</span></span>

## <a name="requirements"></a><span data-ttu-id="91b39-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91b39-143">Requirements</span></span>



| <span data-ttu-id="91b39-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="91b39-144">Requirement</span></span> | <span data-ttu-id="91b39-145">Value</span><span class="sxs-lookup"><span data-stu-id="91b39-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91b39-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91b39-146">Minimum supported client</span></span><br/> | <span data-ttu-id="91b39-147">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="91b39-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91b39-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91b39-148">Minimum supported server</span></span><br/> | <span data-ttu-id="91b39-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="91b39-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="91b39-150">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="91b39-150">End of client support</span></span><br/>    | <span data-ttu-id="91b39-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91b39-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="91b39-152">Producto</span><span class="sxs-lookup"><span data-stu-id="91b39-152">Product</span></span><br/>                  | <span data-ttu-id="91b39-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="91b39-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="91b39-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91b39-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="91b39-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="91b39-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="91b39-156">IID</span><span class="sxs-lookup"><span data-stu-id="91b39-156">IID</span></span><br/>                      | <span data-ttu-id="91b39-157">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="91b39-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="91b39-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="91b39-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b39-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="91b39-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

