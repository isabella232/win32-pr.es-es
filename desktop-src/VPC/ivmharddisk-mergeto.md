---
title: Método Mergeto de IVMHardDisk (VPCCOMInterfaces. h)
description: Combina un disco duro virtual de diferenciación con todos sus elementos primarios.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Método mergeto Virtual PC
- Método mergeto Virtual PC, interfaz IVMHardDisk
- Interfaz IVMHardDisk Virtual PC, método Mergeto
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150381"
---
# <a name="ivmharddiskmergeto-method"></a><span data-ttu-id="f400d-106">IVMHardDisk:: Mergeto (método)</span><span class="sxs-lookup"><span data-stu-id="f400d-106">IVMHardDisk::MergeTo method</span></span>

<span data-ttu-id="f400d-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f400d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f400d-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f400d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f400d-109">Combina un disco duro virtual de diferenciación con todos sus elementos primarios (hasta el disco duro virtual primario raíz incluido) en un nuevo archivo de disco duro.</span><span class="sxs-lookup"><span data-stu-id="f400d-109">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f400d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f400d-110">Syntax</span></span>


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="f400d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f400d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f400d-112">*newDiskImagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f400d-112">*newDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f400d-113">La ruta de acceso a la nueva imagen de disco de destino en la que se combinarán las imágenes de disco seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="f400d-113">The path to the new target disk image where the selected disk images will be merged.</span></span>

</dd> <dt>

<span data-ttu-id="f400d-114">*newDiskImageType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f400d-114">*newDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f400d-115">El tipo de nueva imagen de disco de destino.</span><span class="sxs-lookup"><span data-stu-id="f400d-115">The type of new target disk image.</span></span> <span data-ttu-id="f400d-116">Los tipos de imagen permitidos para la nueva imagen de disco de destino son **vmDiskType \_ Dynamic** y **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="f400d-116">The image types allowed for the new target disk image are **vmDiskType\_Dynamic** and **vmDiskType\_FixedSize**.</span></span> <span data-ttu-id="f400d-117">Para obtener más información, vea [**VMHardDiskType**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="f400d-117">For more information, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="f400d-118">*mergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f400d-118">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f400d-119">Objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la finalización del proceso de combinación.</span><span class="sxs-lookup"><span data-stu-id="f400d-119">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f400d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f400d-120">Return value</span></span>

<span data-ttu-id="f400d-121">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f400d-121">This method can return one of these values.</span></span>



| <span data-ttu-id="f400d-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f400d-122">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="f400d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f400d-123">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f400d-124"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="f400d-125">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f400d-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="f400d-126"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="f400d-127">Un parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="f400d-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="f400d-128"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="f400d-129">El parámetro *newDiskImagePath* está vacío.</span><span class="sxs-lookup"><span data-stu-id="f400d-129">The *newDiskImagePath* parameter is empty.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="f400d-130"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="f400d-131">El sistema no encuentra el archivo especificado por el parámetro *newDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="f400d-131">The system cannot find the file specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="f400d-132"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="f400d-133">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *newDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="f400d-133">The system cannot find the path specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="f400d-134"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="f400d-135">El parámetro *newDiskImagePath* contiene un carácter no válido (uno de los siguientes: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="f400d-135">The *newDiskImagePath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="f400d-136"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="f400d-137">El parámetro *newDiskImagePath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="f400d-137">The *newDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="f400d-138">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="f400d-138">An absolute path is required.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="f400d-139"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="f400d-140">La ruta de acceso especificada por el parámetro *newDiskImagePath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="f400d-140">The path specified by the *newDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="f400d-141">La ruta de acceso debe tener menos de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f400d-141">The path must be less than 260 characters.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="f400d-142"><dt>**HRESULT \_ De \_ Win32 ( \_ \_ infracción de uso compartido de errores)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="f400d-143">El disco duro virtual al que hace referencia este objeto está en uso o el primario de este disco duro virtual está en uso.</span><span class="sxs-lookup"><span data-stu-id="f400d-143">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="f400d-144"><dt>**Máquina virtual \_ E es el \_ \_ \_ \_ tipo de imagen HD**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-144"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="f400d-145">Este error se debe a que la imagen de disco duro virtual a la que hace referencia este objeto [**IVMHardDisk**](ivmharddisk.md) no es una imagen de disco de diferenciación, o bien porque el parámetro *newDiskImageType* no es uno de los valores aceptados, **vmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="f400d-145">This error is caused either because the virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is not a differencing disk image or because the parameter *newDiskImageType* is not one of the accepted values, **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/> |
| <dl> <span data-ttu-id="f400d-146"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="f400d-147">El archivo al que hace referencia el parámetro *newDiskImagePath* ya existe.</span><span class="sxs-lookup"><span data-stu-id="f400d-147">The file referenced by the *newDiskImagePath* parameter already exists.</span></span><br/>                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f400d-148"><dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="f400d-149">El volumen del host no tiene suficiente espacio para fusionar mediante combinación este disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="f400d-149">The host volume does not have enough space to merge this virtual hard disk.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="f400d-150"><dt>**Máquina virtual \_ \_ \_ \_ No \_ se encontró la ruta de acceso principal E**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-150"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="f400d-151">No existe el elemento primario del disco duro virtual al que hace referencia este objeto.</span><span class="sxs-lookup"><span data-stu-id="f400d-151">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="f400d-152"><dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación</span><span class="sxs-lookup"><span data-stu-id="f400d-152"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="f400d-153">No se puede fusionar mediante combinación la imagen de disco duro virtual porque se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="f400d-153">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="f400d-154"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-154"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="f400d-155">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f400d-155">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="f400d-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f400d-156">Requirements</span></span>



| <span data-ttu-id="f400d-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="f400d-157">Requirement</span></span> | <span data-ttu-id="f400d-158">Value</span><span class="sxs-lookup"><span data-stu-id="f400d-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f400d-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f400d-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f400d-160">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f400d-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f400d-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f400d-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f400d-162">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f400d-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f400d-163">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f400d-163">End of client support</span></span><br/>    | <span data-ttu-id="f400d-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f400d-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f400d-165">Producto</span><span class="sxs-lookup"><span data-stu-id="f400d-165">Product</span></span><br/>                  | <span data-ttu-id="f400d-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f400d-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f400d-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f400d-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="f400d-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f400d-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f400d-169">IID</span><span class="sxs-lookup"><span data-stu-id="f400d-169">IID</span></span><br/>                      | <span data-ttu-id="f400d-170">IID \_ IVMHardDisk se define como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="f400d-170">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f400d-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="f400d-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f400d-172">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="f400d-172">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

