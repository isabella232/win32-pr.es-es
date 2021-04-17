---
title: Método IVMVirtualPC RegisterVirtualMachine (VPCCOMInterfaces. h)
description: Registra una configuración de máquina virtual existente y recupera el objeto de máquina virtual.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- Método RegisterVirtualMachine Virtual PC
- Método RegisterVirtualMachine Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método RegisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cc1e27a657eaad70aeec81c0216d1e707fa36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696013"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a><span data-ttu-id="1a0cf-106">IVMVirtualPC:: RegisterVirtualMachine (método)</span><span class="sxs-lookup"><span data-stu-id="1a0cf-106">IVMVirtualPC::RegisterVirtualMachine method</span></span>

<span data-ttu-id="1a0cf-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1a0cf-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1a0cf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1a0cf-109">Registra una configuración de máquina virtual existente y recupera el objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-109">Registers an existing virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a0cf-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a0cf-110">Syntax</span></span>


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="1a0cf-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a0cf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a0cf-112">*configurationName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a0cf-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a0cf-113">El nombre de la máquina virtual que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-113">The name of the virtual machine to be registered.</span></span> <span data-ttu-id="1a0cf-114">La longitud del nombre no puede superar los 80 caracteres y la longitud combinada del nombre y la ruta de acceso no puede superar los caracteres de la **\_ ruta de acceso máxima** (260).</span><span class="sxs-lookup"><span data-stu-id="1a0cf-114">The length of the name cannot exceed 80 characters and the combined length of the name and path cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="1a0cf-115">El nombre especificado puede contener la extensión. VMC.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-115">The specified name may contain the .vmc extension.</span></span> <span data-ttu-id="1a0cf-116">Si este parámetro es **null** o una cadena vacía, el parámetro *configurationPath* debe especificar la ruta de acceso completa al archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="1a0cf-117">*configurationPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a0cf-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a0cf-118">La ruta de acceso a la carpeta que contiene el archivo de configuración existente.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-118">The path to the folder that contains the existing configuration file.</span></span> <span data-ttu-id="1a0cf-119">Si el parámetro *configurationName* es **null** o una cadena vacía, debe especificar la ruta de acceso completa al archivo de configuración existente.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-119">If the *configurationName* parameter is **NULL** or an empty string, this must specify the full path to the existing configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="1a0cf-120">*virtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1a0cf-120">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1a0cf-121">Un puntero a un nuevo objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-121">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a0cf-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a0cf-122">Return value</span></span>

<span data-ttu-id="1a0cf-123">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-123">This method can return one of these values.</span></span>



| <span data-ttu-id="1a0cf-124">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a0cf-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="1a0cf-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a0cf-125">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a0cf-126"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-126"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="1a0cf-127">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-127">The operation was successful.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="1a0cf-128"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-128"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="1a0cf-129">El parámetro *configurationName* o *configurationPath* no es válido o *virtualMachine* es **null**.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-129">The *configurationName* or *configurationPath* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="1a0cf-130"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="1a0cf-131">El sistema no puede encontrar la ruta de acceso especificada por los parámetros *configurationName* y *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="1a0cf-131">The system cannot find the path specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="1a0cf-132"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="1a0cf-133">El sistema no puede encontrar el archivo especificado por los parámetros *configurationName* y *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="1a0cf-133">The system cannot find the file specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="1a0cf-134"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="1a0cf-135">El parámetro *configurationPath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="1a0cf-135">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="1a0cf-136"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="1a0cf-137">El parámetro *configurationPath* del parámetro especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-137">The parameter *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="1a0cf-138">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-138">An absolute path is required.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="1a0cf-139"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="1a0cf-140">La ruta de acceso especificada por los parámetros *configurationName* y *configurationPath* da como resultado una ruta de acceso demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-140">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="1a0cf-141">La longitud combinada de la ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).</span><span class="sxs-lookup"><span data-stu-id="1a0cf-141">The combined length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="1a0cf-142"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="1a0cf-143">Ya existe un archivo de configuración con este nombre en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-143">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="1a0cf-144"><dt>**Máquina virtual \_ E \_ nombre de configuración \_ \_ demasiado \_ largo**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-144"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="1a0cf-145">El parámetro *configurationName* supera los 80 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-145">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="1a0cf-146"><dt>**Máquina virtual \_ E \_ nombre de configuración de 0xA0040402 \_ \_ \_ Char no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-146"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="1a0cf-147">El parámetro *configurationName* contiene un carácter no válido (uno de " \* ?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="1a0cf-147">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="1a0cf-148"><dt>**Máquina virtual \_ E \_ configuración \_ \_ nombre duplicado**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-148"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="1a0cf-149">Ya hay una máquina virtual con este nombre.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-149">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="1a0cf-150"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-150"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="1a0cf-151">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="1a0cf-151">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="1a0cf-152"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-152"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="1a0cf-153">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-153">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="1a0cf-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a0cf-154">Remarks</span></span>

<span data-ttu-id="1a0cf-155">Los nombres de las máquinas virtuales no distinguen mayúsculas de minúsculas, por ejemplo, "MyVM" y "MyVM" hacen referencia a la misma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1a0cf-155">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a0cf-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a0cf-156">Requirements</span></span>



| <span data-ttu-id="1a0cf-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a0cf-157">Requirement</span></span> | <span data-ttu-id="1a0cf-158">Value</span><span class="sxs-lookup"><span data-stu-id="1a0cf-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a0cf-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a0cf-159">Minimum supported client</span></span><br/> | <span data-ttu-id="1a0cf-160">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a0cf-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a0cf-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a0cf-161">Minimum supported server</span></span><br/> | <span data-ttu-id="1a0cf-162">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1a0cf-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1a0cf-163">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1a0cf-163">End of client support</span></span><br/>    | <span data-ttu-id="1a0cf-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1a0cf-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1a0cf-165">Producto</span><span class="sxs-lookup"><span data-stu-id="1a0cf-165">Product</span></span><br/>                  | <span data-ttu-id="1a0cf-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1a0cf-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1a0cf-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a0cf-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a0cf-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a0cf-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1a0cf-169">IID</span><span class="sxs-lookup"><span data-stu-id="1a0cf-169">IID</span></span><br/>                      | <span data-ttu-id="1a0cf-170">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="1a0cf-170">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="1a0cf-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a0cf-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a0cf-172">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="1a0cf-172">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

