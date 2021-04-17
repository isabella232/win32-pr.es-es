---
title: Método IVMVirtualPC CreateDifferencingVirtualHardDisk (VPCCOMInterfaces. h)
description: Crea un disco duro virtual de diferenciación.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- Método CreateDifferencingVirtualHardDisk Virtual PC
- Método CreateDifferencingVirtualHardDisk Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método CreateDifferencingVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bab178d64008b236988bfb723bd75a09a7edaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696003"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a><span data-ttu-id="e6600-106">IVMVirtualPC:: CreateDifferencingVirtualHardDisk (método)</span><span class="sxs-lookup"><span data-stu-id="e6600-106">IVMVirtualPC::CreateDifferencingVirtualHardDisk method</span></span>

<span data-ttu-id="e6600-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6600-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e6600-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e6600-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e6600-109">Crea un disco duro virtual de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="e6600-109">Creates a differencing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6600-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6600-110">Syntax</span></span>


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="e6600-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6600-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6600-112">*imagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6600-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6600-113">Ruta de acceso al nuevo archivo de imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="e6600-113">The path to the new disk image file.</span></span> <span data-ttu-id="e6600-114">Si no existe, se creará la carpeta contenedora.</span><span class="sxs-lookup"><span data-stu-id="e6600-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="e6600-115">*parentPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6600-115">*parentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6600-116">Ruta de acceso al archivo de imagen de disco principal.</span><span class="sxs-lookup"><span data-stu-id="e6600-116">The path to the parent disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="e6600-117">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e6600-117">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e6600-118">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la creación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="e6600-118">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6600-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6600-119">Return value</span></span>

<span data-ttu-id="e6600-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e6600-120">This method can return one of these values.</span></span>



| <span data-ttu-id="e6600-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6600-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="e6600-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6600-122">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6600-123"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="e6600-124">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e6600-124">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="e6600-125"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="e6600-126">Un parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="e6600-126">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="e6600-127"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="e6600-128">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *imagePath* o *parentPath* .</span><span class="sxs-lookup"><span data-stu-id="e6600-128">The system cannot find the path specified by the *imagePath* or *parentPath* parameter.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="e6600-129"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ unidad no válida)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="e6600-130">El archivo especificado por el parámetro *imagePath* se encuentra en un CD-ROM o DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e6600-130">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="e6600-131"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="e6600-132">El parámetro *imagePath* o *parentPath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="e6600-132">The *imagePath* or *parentPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="e6600-133"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="e6600-134">El parámetro *imagePath* y *parentPath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="e6600-134">Both the *imagePath* and *parentPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="e6600-135">Al menos uno de los parámetros debe ser una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="e6600-135">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="e6600-136"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="e6600-137">La ruta de acceso especificada por los parámetros *imagePath* o *parentPath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="e6600-137">The path specified by the *imagePath* or *parentPath* parameters is too long.</span></span> <span data-ttu-id="e6600-138">La longitud de la ruta de acceso debe ser inferior a 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e6600-138">The length of the path must be less than 260 characters.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="e6600-139"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="e6600-140">El archivo al que hace referencia el parámetro *imagePath* ya existe.</span><span class="sxs-lookup"><span data-stu-id="e6600-140">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="e6600-141"><dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="e6600-142">La imagen de disco duro virtual de expansión dinámica necesita al menos 8 MB de espacio libre en el volumen del host.</span><span class="sxs-lookup"><span data-stu-id="e6600-142">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="e6600-143"><dt>**Máquina virtual \_ E \_ tamaño de imagen \_ \_ demasiado \_ grande**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-143"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="e6600-144">El *tamaño* del parámetro debe ser inferior a 2.088.960 MB.</span><span class="sxs-lookup"><span data-stu-id="e6600-144">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="e6600-145">Si el formato es FAT16, el tamaño debe ser inferior a 2000 MB.</span><span class="sxs-lookup"><span data-stu-id="e6600-145">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="e6600-146"><dt>**Máquina virtual \_ E \_ tamaño de imagen \_ \_ demasiado \_ pequeño**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="e6600-147">Las imágenes de disco duro virtual con formato FAT16 y sin formato deben ser de al menos 3 MB.</span><span class="sxs-lookup"><span data-stu-id="e6600-147">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="e6600-148">Las imágenes de disco duro virtual con formato FAT32 deben ser de al menos 514 MB.</span><span class="sxs-lookup"><span data-stu-id="e6600-148">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="e6600-149"><dt>**Máquina virtual \_ El \_ archivo E \_ es demasiado \_ grande \_ para el \_ volumen**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-149"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="e6600-150">El volumen del host no puede admitir un archivo este tamaño si la imagen de disco duro virtual de expansión dinámica se expande hasta su límite completo.</span><span class="sxs-lookup"><span data-stu-id="e6600-150">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="e6600-151">El tamaño de archivo máximo para un volumen FAT32 es 4 GB.</span><span class="sxs-lookup"><span data-stu-id="e6600-151">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="e6600-152">El tamaño de archivo máximo para un volumen FAT16 es 2 GB.</span><span class="sxs-lookup"><span data-stu-id="e6600-152">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="e6600-153"><dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación</span><span class="sxs-lookup"><span data-stu-id="e6600-153"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="e6600-154">No se puede crear el disco duro virtual después de que la aplicación haya empezado a cerrarse.</span><span class="sxs-lookup"><span data-stu-id="e6600-154">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="e6600-155"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-155"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="e6600-156">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="e6600-156">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="e6600-157"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-157"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="e6600-158">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="e6600-158">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="e6600-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6600-159">Remarks</span></span>

<span data-ttu-id="e6600-160">Aunque *imagePath* o *parentPath* puede ser una ruta de acceso relativa, al menos uno de estos valores debe ser una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="e6600-160">Although either *imagePath* or *parentPath* can be a relative path, at least one of these must be an absolute path.</span></span> <span data-ttu-id="e6600-161">Si un parámetro de ruta de acceso es una ruta de acceso relativa, se supone que es relativo al otro parámetro de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="e6600-161">If one path parameter is a relative path, it is assumed to be relative to the other path parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6600-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6600-162">Requirements</span></span>



| <span data-ttu-id="e6600-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6600-163">Requirement</span></span> | <span data-ttu-id="e6600-164">Value</span><span class="sxs-lookup"><span data-stu-id="e6600-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6600-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6600-165">Minimum supported client</span></span><br/> | <span data-ttu-id="e6600-166">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6600-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6600-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6600-167">Minimum supported server</span></span><br/> | <span data-ttu-id="e6600-168">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e6600-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e6600-169">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e6600-169">End of client support</span></span><br/>    | <span data-ttu-id="e6600-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6600-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e6600-171">Producto</span><span class="sxs-lookup"><span data-stu-id="e6600-171">Product</span></span><br/>                  | <span data-ttu-id="e6600-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e6600-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e6600-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6600-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6600-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6600-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e6600-175">IID</span><span class="sxs-lookup"><span data-stu-id="e6600-175">IID</span></span><br/>                      | <span data-ttu-id="e6600-176">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e6600-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e6600-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6600-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6600-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="e6600-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

