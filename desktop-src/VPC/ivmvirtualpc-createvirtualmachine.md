---
title: Método IVMVirtualPC CreateVirtualMachine (VPCCOMInterfaces. h)
description: Crea una nueva configuración de máquina virtual y recupera el objeto de máquina virtual.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- Método CreateVirtualMachine Virtual PC
- Método CreateVirtualMachine Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método CreateVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492046"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a><span data-ttu-id="6242e-106">IVMVirtualPC:: CreateVirtualMachine (método)</span><span class="sxs-lookup"><span data-stu-id="6242e-106">IVMVirtualPC::CreateVirtualMachine method</span></span>

<span data-ttu-id="6242e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6242e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6242e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6242e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6242e-109">Crea una nueva configuración de máquina virtual y recupera el objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6242e-109">Creates a new virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6242e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6242e-110">Syntax</span></span>


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="6242e-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6242e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6242e-112">*configurationName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6242e-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6242e-113">Nombre de la máquina virtual que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="6242e-113">The name of the virtual machine to be created.</span></span> <span data-ttu-id="6242e-114">La longitud del nombre no puede superar los 80 caracteres y la longitud combinada del nombre y la ruta de acceso a los archivos VMC y VMCX no pueden superar los caracteres de la **\_ ruta de acceso máxima** (260).</span><span class="sxs-lookup"><span data-stu-id="6242e-114">The length of the name cannot exceed 80 characters and the combined length of the name and path to VMC and VMCX files cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="6242e-115">Las extensiones de nombre de archivo. VMC y. vmcx se anexarán al final del nombre de la máquina virtual cuando se creen los archivos de configuración.</span><span class="sxs-lookup"><span data-stu-id="6242e-115">The file name extensions .vmc and .vmcx will be appended to the end of the virtual machine name when the configuration files are created.</span></span> <span data-ttu-id="6242e-116">Si este parámetro es **null** o una cadena vacía, el parámetro *configurationPath* debe especificar la ruta de acceso completa al archivo VMC.</span><span class="sxs-lookup"><span data-stu-id="6242e-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the VMC file.</span></span>

</dd> <dt>

<span data-ttu-id="6242e-117">*configurationPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6242e-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6242e-118">La ruta de acceso a la carpeta que contendrá el archivo VMC.</span><span class="sxs-lookup"><span data-stu-id="6242e-118">The path to the folder that will contain the VMC file.</span></span> <span data-ttu-id="6242e-119">Esta carpeta se creará si no existe.</span><span class="sxs-lookup"><span data-stu-id="6242e-119">This folder will be created if it does not exist.</span></span> <span data-ttu-id="6242e-120">Si *configurationName* es **null** o una cadena vacía, debe especificar la ruta de acceso completa del nuevo archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="6242e-120">If *configurationName* is **NULL** or an empty string, this must specify the full path of the new configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="6242e-121">*virtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6242e-121">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6242e-122">Un puntero a un nuevo objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6242e-122">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6242e-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6242e-123">Return value</span></span>

<span data-ttu-id="6242e-124">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6242e-124">This method can return one of these values.</span></span>



| <span data-ttu-id="6242e-125">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6242e-125">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="6242e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="6242e-126">Description</span></span>                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6242e-127"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-127"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="6242e-128">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6242e-128">The operation was successful.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="6242e-129"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-129"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="6242e-130">El parámetro *configurationName* o *configurationPath* no es válido o el parámetro *virtualMachine* es **null**.</span><span class="sxs-lookup"><span data-stu-id="6242e-130">The *configurationName* or *configurationPath* parameter is not valid, or the *virtualMachine* parameter is **NULL**.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="6242e-131"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="6242e-132">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="6242e-132">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="6242e-133"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="6242e-134">El parámetro *configurationPath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="6242e-134">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="6242e-135"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="6242e-136">El parámetro *configurationPath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="6242e-136">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="6242e-137">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="6242e-137">An absolute path is required.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6242e-138"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="6242e-139">La ruta de acceso especificada por los parámetros *configurationName* y *configurationPath* da como resultado una ruta de acceso demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="6242e-139">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="6242e-140">La longitud total de la ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).</span><span class="sxs-lookup"><span data-stu-id="6242e-140">The total length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="6242e-141"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="6242e-142">Ya existe un archivo de configuración con este nombre en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="6242e-142">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="6242e-143"><dt>**Máquina virtual \_ E \_ configuración \_ sin \_ nombre**</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-143"><dt>**VM\_E\_CONFIG\_NO\_NAME**</dt> <dt>0xA0040400</dt></span></span> </dl>                       | <span data-ttu-id="6242e-144">El parámetro *configurationName* está vacío.</span><span class="sxs-lookup"><span data-stu-id="6242e-144">The *configurationName* parameter is empty.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="6242e-145"><dt>**Máquina virtual \_ E \_ nombre de configuración \_ \_ demasiado \_ largo**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-145"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="6242e-146">El parámetro *configurationName* supera los 80 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="6242e-146">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="6242e-147"><dt>**Máquina virtual \_ E \_ nombre de configuración de 0xA0040402 \_ \_ \_ Char no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6242e-147"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="6242e-148">El parámetro *configurationName* contiene un carácter no válido (uno de " \* ?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="6242e-148">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="6242e-149"><dt>**Máquina virtual \_ E \_ configuración \_ \_ nombre duplicado**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-149"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="6242e-150">Ya hay una máquina virtual con este nombre.</span><span class="sxs-lookup"><span data-stu-id="6242e-150">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="6242e-151"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-151"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="6242e-152">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="6242e-152">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="6242e-153"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="6242e-154">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="6242e-154">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="6242e-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6242e-155">Remarks</span></span>

<span data-ttu-id="6242e-156">Los nombres de las máquinas virtuales no distinguen mayúsculas de minúsculas, por ejemplo, "MyVM" y "MyVM" hacen referencia a la misma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6242e-156">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="6242e-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6242e-157">Requirements</span></span>



| <span data-ttu-id="6242e-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="6242e-158">Requirement</span></span> | <span data-ttu-id="6242e-159">Value</span><span class="sxs-lookup"><span data-stu-id="6242e-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6242e-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6242e-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6242e-161">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6242e-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6242e-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6242e-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6242e-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6242e-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6242e-164">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6242e-164">End of client support</span></span><br/>    | <span data-ttu-id="6242e-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6242e-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6242e-166">Producto</span><span class="sxs-lookup"><span data-stu-id="6242e-166">Product</span></span><br/>                  | <span data-ttu-id="6242e-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6242e-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6242e-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6242e-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="6242e-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6242e-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6242e-170">IID</span><span class="sxs-lookup"><span data-stu-id="6242e-170">IID</span></span><br/>                      | <span data-ttu-id="6242e-171">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="6242e-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6242e-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="6242e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6242e-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="6242e-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

