---
title: Método IVMVirtualPC CreateFixedVirtualHardDisk (VPCCOMInterfaces. h)
description: Crea un disco duro virtual de tamaño fijo.
ms.assetid: c58a7f2c-efd7-4a39-9ce5-617baa82084b
keywords:
- Método CreateFixedVirtualHardDisk Virtual PC
- Método CreateFixedVirtualHardDisk Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método CreateFixedVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFixedVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c1c260611ba3a8b55f87f23d0957c53a304a471
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150379"
---
# <a name="ivmvirtualpccreatefixedvirtualharddisk-method"></a><span data-ttu-id="139f7-106">IVMVirtualPC:: CreateFixedVirtualHardDisk (método)</span><span class="sxs-lookup"><span data-stu-id="139f7-106">IVMVirtualPC::CreateFixedVirtualHardDisk method</span></span>

<span data-ttu-id="139f7-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="139f7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="139f7-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="139f7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="139f7-109">Crea un disco duro virtual de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="139f7-109">Creates a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="139f7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="139f7-110">Syntax</span></span>


```C++
HRESULT CreateFixedVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="139f7-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="139f7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="139f7-112">*imagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="139f7-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="139f7-113">Ruta de acceso completa al nuevo archivo de imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="139f7-113">The full path to the new disk image file.</span></span> <span data-ttu-id="139f7-114">Si no existe, se creará la carpeta contenedora.</span><span class="sxs-lookup"><span data-stu-id="139f7-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="139f7-115">*tamaño* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="139f7-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="139f7-116">Tamaño, en megabytes, de la imagen.</span><span class="sxs-lookup"><span data-stu-id="139f7-116">The size, in megabytes, of the image.</span></span> <span data-ttu-id="139f7-117">El tamaño máximo es 2.088.960 MB (2040GB).</span><span class="sxs-lookup"><span data-stu-id="139f7-117">Maximum size is 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="139f7-118">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="139f7-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="139f7-119">Un objeto [**IVMTask**](ivmtask.md) que se usa para realizar el seguimiento de la creación de la imagen.</span><span class="sxs-lookup"><span data-stu-id="139f7-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="139f7-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="139f7-120">Return value</span></span>

<span data-ttu-id="139f7-121">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="139f7-121">This method can return one of these values.</span></span>



| <span data-ttu-id="139f7-122">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="139f7-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="139f7-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="139f7-123">Description</span></span>                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="139f7-124"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="139f7-125">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="139f7-125">The operation was successful.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="139f7-126"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="139f7-127">Un parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="139f7-127">A parameter is **NULL**.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="139f7-128"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="139f7-129">El parámetro de *tamaño* es menor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="139f7-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="139f7-130"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="139f7-131">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="139f7-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="139f7-132"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ unidad no válida)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="139f7-133">El archivo especificado por el parámetro *imagePath* se encuentra en un CD-ROM o DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="139f7-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="139f7-134"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="139f7-135">El parámetro *imagePath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="139f7-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="139f7-136"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="139f7-137">El parámetro *imagePath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="139f7-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="139f7-138">Al menos uno de los parámetros debe ser una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="139f7-138">At least one of the parameters must be an absolute path.</span></span><br/>                         |
| <dl> <span data-ttu-id="139f7-139"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="139f7-140">La ruta de acceso especificada por el parámetro *imagePath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="139f7-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="139f7-141">La longitud de la ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).</span><span class="sxs-lookup"><span data-stu-id="139f7-141">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/>                |
| <dl> <span data-ttu-id="139f7-142"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="139f7-143">El archivo al que hace referencia el parámetro *imagePath* ya existe.</span><span class="sxs-lookup"><span data-stu-id="139f7-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="139f7-144"><dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="139f7-145">La imagen de disco duro virtual de expansión dinámica necesita al menos 8 MB de espacio libre en el volumen del host.</span><span class="sxs-lookup"><span data-stu-id="139f7-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="139f7-146"><dt>**Máquina virtual \_ E \_ tamaño de imagen \_ \_ demasiado \_ grande**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="139f7-147">El parámetro de *tamaño* debe ser inferior a 2.088.960 MB.</span><span class="sxs-lookup"><span data-stu-id="139f7-147">The *size* parameter must be less than 2,088,960 MB.</span></span> <span data-ttu-id="139f7-148">Si el formato es FAT16, el parámetro de *tamaño* debe ser inferior a 2000 MB.</span><span class="sxs-lookup"><span data-stu-id="139f7-148">If the format is FAT16, then the *size* parameter must be less than 2000 MB.</span></span><br/>                    |
| <dl> <span data-ttu-id="139f7-149"><dt>**Máquina virtual \_ E \_ tamaño de imagen \_ \_ demasiado \_ pequeño**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="139f7-150">Las imágenes de disco duro virtual con formato FAT16 y sin formato deben ser de al menos 3 MB.</span><span class="sxs-lookup"><span data-stu-id="139f7-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="139f7-151">Las imágenes de disco duro virtual con formato FAT32 deben ser de al menos 514 MB.</span><span class="sxs-lookup"><span data-stu-id="139f7-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>    |
| <dl> <span data-ttu-id="139f7-152"><dt>**Máquina virtual \_ El \_ archivo E \_ es demasiado \_ grande \_ para el \_ volumen**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="139f7-153">El volumen del host no admite el tamaño de un archivo.</span><span class="sxs-lookup"><span data-stu-id="139f7-153">The host volume cannot support a file this size.</span></span> <span data-ttu-id="139f7-154">El tamaño de archivo máximo para un volumen FAT32 es 4 GB.</span><span class="sxs-lookup"><span data-stu-id="139f7-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="139f7-155">El tamaño de archivo máximo para un volumen FAT16 es 2 GB.</span><span class="sxs-lookup"><span data-stu-id="139f7-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="139f7-156"><dt>**Máquina virtual \_ E \_ \_ \_**</dt> <dt>0xA0040209</dt> de la aplicación</span><span class="sxs-lookup"><span data-stu-id="139f7-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="139f7-157">No se puede crear el disco duro virtual después de que la aplicación haya empezado a cerrarse.</span><span class="sxs-lookup"><span data-stu-id="139f7-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="139f7-158"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="139f7-159">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="139f7-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="139f7-160"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="139f7-161">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="139f7-161">An unexpected error has occurred.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="139f7-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="139f7-162">Requirements</span></span>



| <span data-ttu-id="139f7-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="139f7-163">Requirement</span></span> | <span data-ttu-id="139f7-164">Value</span><span class="sxs-lookup"><span data-stu-id="139f7-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="139f7-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="139f7-165">Minimum supported client</span></span><br/> | <span data-ttu-id="139f7-166">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="139f7-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="139f7-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="139f7-167">Minimum supported server</span></span><br/> | <span data-ttu-id="139f7-168">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="139f7-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="139f7-169">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="139f7-169">End of client support</span></span><br/>    | <span data-ttu-id="139f7-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="139f7-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="139f7-171">Producto</span><span class="sxs-lookup"><span data-stu-id="139f7-171">Product</span></span><br/>                  | <span data-ttu-id="139f7-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="139f7-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="139f7-173">Encabezado</span><span class="sxs-lookup"><span data-stu-id="139f7-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="139f7-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="139f7-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="139f7-175">IID</span><span class="sxs-lookup"><span data-stu-id="139f7-175">IID</span></span><br/>                      | <span data-ttu-id="139f7-176">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="139f7-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="139f7-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="139f7-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="139f7-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="139f7-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

