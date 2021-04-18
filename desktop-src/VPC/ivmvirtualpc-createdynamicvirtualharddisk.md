---
title: Método IVMVirtualPC CreateDynamicVirtualHardDisk (VPCCOMInterfaces. h)
description: Crea un disco duro virtual de cambio de tamaño dinámico.
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- Método CreateDynamicVirtualHardDisk Virtual PC
- Método CreateDynamicVirtualHardDisk Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método CreateDynamicVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDynamicVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d245072fd5b3135decd814a29dd8a87d2b6a956
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422619"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a><span data-ttu-id="23a44-106">IVMVirtualPC:: CreateDynamicVirtualHardDisk (método)</span><span class="sxs-lookup"><span data-stu-id="23a44-106">IVMVirtualPC::CreateDynamicVirtualHardDisk method</span></span>

<span data-ttu-id="23a44-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="23a44-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="23a44-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="23a44-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="23a44-109">Crea un disco duro virtual de cambio de tamaño dinámico.</span><span class="sxs-lookup"><span data-stu-id="23a44-109">Creates a dynamically resizing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a44-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23a44-110">Syntax</span></span>


```C++
HRESULT CreateDynamicVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="23a44-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23a44-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23a44-112">*imagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23a44-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a44-113">Ruta de acceso completa al nuevo archivo de imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="23a44-113">The full path to the new disk image file.</span></span> <span data-ttu-id="23a44-114">Si no existe, se creará la carpeta contenedora.</span><span class="sxs-lookup"><span data-stu-id="23a44-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="23a44-115">*tamaño* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="23a44-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a44-116">Tamaño de la imagen, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="23a44-116">The size of the image, in megabytes.</span></span> <span data-ttu-id="23a44-117">Este valor puede ser como máximo 2.088.960 MB (2040GB).</span><span class="sxs-lookup"><span data-stu-id="23a44-117">This value can be at most 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="23a44-118">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="23a44-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="23a44-119">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la creación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="23a44-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23a44-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23a44-120">Return value</span></span>

<span data-ttu-id="23a44-121">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="23a44-121">This method can return one of these values.</span></span>



| <span data-ttu-id="23a44-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23a44-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="23a44-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="23a44-123">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23a44-124"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="23a44-125">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="23a44-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="23a44-126"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="23a44-127">Un parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="23a44-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="23a44-128"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="23a44-129">El parámetro de *tamaño* es menor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="23a44-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="23a44-130"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="23a44-131">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="23a44-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="23a44-132"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ unidad no válida)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="23a44-133">El archivo especificado por el parámetro *imagePath* se encuentra en un CD-ROM o DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="23a44-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="23a44-134"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="23a44-135">El parámetro *imagePath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="23a44-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="23a44-136"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="23a44-137">El parámetro *imagePath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="23a44-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="23a44-138">Al menos uno de los parámetros debe ser una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="23a44-138">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="23a44-139"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="23a44-140">La ruta de acceso especificada por el parámetro *imagePath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="23a44-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="23a44-141">La longitud de la ruta de acceso debe ser inferior a 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="23a44-141">The length of the path must be less than 260 characters.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="23a44-142"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="23a44-143">El archivo al que hace referencia el parámetro *imagePath* ya existe.</span><span class="sxs-lookup"><span data-stu-id="23a44-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="23a44-144"><dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="23a44-145">La imagen de disco duro virtual de expansión dinámica necesita al menos 8 MB de espacio libre en el volumen del host.</span><span class="sxs-lookup"><span data-stu-id="23a44-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="23a44-146"><dt>**Máquina virtual \_ E \_ tamaño de imagen \_ \_ demasiado \_ grande**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="23a44-147">El *tamaño* del parámetro debe ser inferior a 2.088.960 MB.</span><span class="sxs-lookup"><span data-stu-id="23a44-147">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="23a44-148">Si el formato es FAT16, el tamaño debe ser inferior a 2000 MB.</span><span class="sxs-lookup"><span data-stu-id="23a44-148">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="23a44-149"><dt>**Máquina virtual \_ E \_ tamaño de imagen \_ \_ demasiado \_ pequeño**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="23a44-150">Las imágenes de disco duro virtual con formato FAT16 y sin formato deben ser de al menos 3 MB.</span><span class="sxs-lookup"><span data-stu-id="23a44-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="23a44-151">Las imágenes de disco duro virtual con formato FAT32 deben ser de al menos 514 MB.</span><span class="sxs-lookup"><span data-stu-id="23a44-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="23a44-152"><dt>**Máquina virtual \_ El \_ archivo E \_ es demasiado \_ grande \_ para el \_ volumen**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="23a44-153">El volumen del host no puede admitir un archivo este tamaño si la imagen de disco duro virtual de expansión dinámica se expande hasta su límite completo.</span><span class="sxs-lookup"><span data-stu-id="23a44-153">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="23a44-154">El tamaño de archivo máximo para un volumen FAT32 es 4 GB.</span><span class="sxs-lookup"><span data-stu-id="23a44-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="23a44-155">El tamaño de archivo máximo para un volumen FAT16 es 2 GB.</span><span class="sxs-lookup"><span data-stu-id="23a44-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="23a44-156"><dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación</span><span class="sxs-lookup"><span data-stu-id="23a44-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="23a44-157">No se puede crear el disco duro virtual después de que la aplicación haya empezado a cerrarse.</span><span class="sxs-lookup"><span data-stu-id="23a44-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="23a44-158"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="23a44-159">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="23a44-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="23a44-160"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="23a44-161">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="23a44-161">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="23a44-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23a44-162">Requirements</span></span>



| <span data-ttu-id="23a44-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="23a44-163">Requirement</span></span> | <span data-ttu-id="23a44-164">Value</span><span class="sxs-lookup"><span data-stu-id="23a44-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="23a44-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23a44-165">Minimum supported client</span></span><br/> | <span data-ttu-id="23a44-166">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="23a44-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23a44-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23a44-167">Minimum supported server</span></span><br/> | <span data-ttu-id="23a44-168">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="23a44-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="23a44-169">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="23a44-169">End of client support</span></span><br/>    | <span data-ttu-id="23a44-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="23a44-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="23a44-171">Producto</span><span class="sxs-lookup"><span data-stu-id="23a44-171">Product</span></span><br/>                  | <span data-ttu-id="23a44-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="23a44-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="23a44-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23a44-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="23a44-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="23a44-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="23a44-175">IID</span><span class="sxs-lookup"><span data-stu-id="23a44-175">IID</span></span><br/>                      | <span data-ttu-id="23a44-176">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="23a44-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="23a44-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="23a44-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a44-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="23a44-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

