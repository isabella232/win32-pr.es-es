---
title: Método Convert de IVMHardDisk (VPCCOMInterfaces. h)
description: Convierte un disco duro virtual de tamaño fijo en un disco duro virtual de expansión dinámica o convierte un disco duro virtual de expansión dinámica en un disco duro virtual de tamaño fijo.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Convertir el método en Virtual PC
- Método Convert Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, método Convert
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492695"
---
# <a name="ivmharddiskconvert-method"></a><span data-ttu-id="3a933-106">IVMHardDisk:: Convert (método)</span><span class="sxs-lookup"><span data-stu-id="3a933-106">IVMHardDisk::Convert method</span></span>

<span data-ttu-id="3a933-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3a933-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3a933-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3a933-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3a933-109">Convierte un disco duro virtual de tamaño fijo en un disco duro virtual de expansión dinámica o convierte un disco duro virtual de expansión dinámica en un disco duro virtual de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="3a933-109">Converts a fixed-size virtual hard disk to a dynamically expanding virtual hard disk or converts a dynamically expanding virtual hard disk to a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a933-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a933-110">Syntax</span></span>


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a><span data-ttu-id="3a933-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a933-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a933-112">*convertedDiskImagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a933-112">*convertedDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a933-113">Ruta de acceso al archivo de imagen de disco de destino.</span><span class="sxs-lookup"><span data-stu-id="3a933-113">The path to the target disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="3a933-114">*convertedDiskImageType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3a933-114">*convertedDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a933-115">El tipo de la imagen de disco de destino.</span><span class="sxs-lookup"><span data-stu-id="3a933-115">The type of the target disk image.</span></span> <span data-ttu-id="3a933-116">Para obtener una lista de valores, vea [**VMHardDiskType**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="3a933-116">For a list of values, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a933-117">*convertTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3a933-117">*convertTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3a933-118">Objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la finalización del proceso de conversión.</span><span class="sxs-lookup"><span data-stu-id="3a933-118">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the conversion process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a933-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a933-119">Return value</span></span>

<span data-ttu-id="3a933-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3a933-120">This method can return one of these values.</span></span>



| <span data-ttu-id="3a933-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a933-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="3a933-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a933-122">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3a933-123"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="3a933-124">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3a933-124">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="3a933-125"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="3a933-126">El parámetro *convertedDiskImagePath* está vacío o falta la extensión. vhd en el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="3a933-126">The *convertedDiskImagePath* parameter is empty or missing the .vhd extension on the file name.</span></span><br/>                                      |
| <dl> <span data-ttu-id="3a933-127"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-127"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="3a933-128">Un parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="3a933-128">A parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="3a933-129"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="3a933-130">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *convertedDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="3a933-130">The system cannot find the path specified by the *convertedDiskImagePath* parameter.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="3a933-131"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="3a933-132">El parámetro *convertedDiskImagePath* contiene un carácter no válido (uno de " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="3a933-132">The *convertedDiskImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="3a933-133"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="3a933-134">El parámetro *convertedDiskImagePath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="3a933-134">The *convertedDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="3a933-135">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="3a933-135">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="3a933-136"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="3a933-137">La ruta de acceso especificada por el parámetro *convertedDiskImagePath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="3a933-137">The path specified by the *convertedDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="3a933-138">La ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).</span><span class="sxs-lookup"><span data-stu-id="3a933-138">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="3a933-139"><dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="3a933-140">El disco duro virtual al que hace referencia este objeto está en uso o el primario de este disco duro virtual está en uso.</span><span class="sxs-lookup"><span data-stu-id="3a933-140">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                  |
| <dl> <span data-ttu-id="3a933-141"><dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="3a933-142">El volumen del host no tiene suficiente espacio para convertir este disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="3a933-142">The host volume does not have enough space to convert this virtual hard disk.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3a933-143"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-143"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="3a933-144">El archivo al que hace referencia el parámetro *convertedDiskImagePath* ya existe.</span><span class="sxs-lookup"><span data-stu-id="3a933-144">The file referenced by the *convertedDiskImagePath* parameter already exists.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3a933-145"><dt>**Máquina virtual \_ E es el \_ \_ \_ \_ tipo de imagen HD**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-145"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="3a933-146">El parámetro *convertedDiskImagePath* debe ser **VmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="3a933-146">The *convertedDiskImagePath* parameter must be either **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/>                          |
| <dl> <span data-ttu-id="3a933-147"><dt>**Máquina virtual \_ E 0xA0040682 de \_ \_ \_ archivo HD no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3a933-147"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="3a933-148">Parece que la imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) no es una imagen válida.</span><span class="sxs-lookup"><span data-stu-id="3a933-148">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |
| <dl> <span data-ttu-id="3a933-149"><dt>**Máquina virtual \_ \_ \_ \_ No \_ se encontró la ruta de acceso principal E**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-149"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="3a933-150">No existe el elemento primario del disco duro virtual al que hace referencia este objeto.</span><span class="sxs-lookup"><span data-stu-id="3a933-150">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3a933-151"><dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación</span><span class="sxs-lookup"><span data-stu-id="3a933-151"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="3a933-152">No se puede convertir la imagen de disco duro virtual porque la aplicación se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="3a933-152">The virtual hard disk image cannot be converted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="3a933-153"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="3a933-154">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="3a933-154">An unexpected error has occurred.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="3a933-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a933-155">Remarks</span></span>

<span data-ttu-id="3a933-156">El archivo de código fuente se deja intacto después del proceso de conversión.</span><span class="sxs-lookup"><span data-stu-id="3a933-156">The source file is left intact after the conversion process.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a933-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a933-157">Requirements</span></span>



| <span data-ttu-id="3a933-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a933-158">Requirement</span></span> | <span data-ttu-id="3a933-159">Value</span><span class="sxs-lookup"><span data-stu-id="3a933-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a933-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a933-160">Minimum supported client</span></span><br/> | <span data-ttu-id="3a933-161">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a933-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a933-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a933-162">Minimum supported server</span></span><br/> | <span data-ttu-id="3a933-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3a933-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3a933-164">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3a933-164">End of client support</span></span><br/>    | <span data-ttu-id="3a933-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a933-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3a933-166">Producto</span><span class="sxs-lookup"><span data-stu-id="3a933-166">Product</span></span><br/>                  | <span data-ttu-id="3a933-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3a933-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3a933-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a933-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a933-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a933-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3a933-170">IID</span><span class="sxs-lookup"><span data-stu-id="3a933-170">IID</span></span><br/>                      | <span data-ttu-id="3a933-171">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="3a933-171">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3a933-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a933-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a933-173">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="3a933-173">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

