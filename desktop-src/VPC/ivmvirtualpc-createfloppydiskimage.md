---
title: Método IVMVirtualPC CreateFloppyDiskImage (VPCCOMInterfaces. h)
description: Crea un archivo de imagen de disquete.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- Método CreateFloppyDiskImage Virtual PC
- Método CreateFloppyDiskImage Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método CreateFloppyDiskImage
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492041"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a><span data-ttu-id="523cc-106">IVMVirtualPC:: CreateFloppyDiskImage (método)</span><span class="sxs-lookup"><span data-stu-id="523cc-106">IVMVirtualPC::CreateFloppyDiskImage method</span></span>

<span data-ttu-id="523cc-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="523cc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="523cc-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="523cc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="523cc-109">Crea un archivo de imagen de disquete.</span><span class="sxs-lookup"><span data-stu-id="523cc-109">Creates a floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="523cc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="523cc-110">Syntax</span></span>


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a><span data-ttu-id="523cc-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="523cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="523cc-112">*imagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="523cc-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="523cc-113">Ruta de acceso completa al nuevo archivo de imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="523cc-113">The full path to the new disk image file.</span></span> <span data-ttu-id="523cc-114">Si no existe, se creará la carpeta contenedora.</span><span class="sxs-lookup"><span data-stu-id="523cc-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="523cc-115">*imageType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="523cc-115">*imageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="523cc-116">El tipo de imagen de disquete que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="523cc-116">The type of floppy disk image to create.</span></span> <span data-ttu-id="523cc-117">Solo se admiten **vmFloppyDiskImage \_ LowDensity** (1) y **vmFloppyDiskImage \_ HighDensity** (2).</span><span class="sxs-lookup"><span data-stu-id="523cc-117">Only **vmFloppyDiskImage\_LowDensity** (1) and **vmFloppyDiskImage\_HighDensity** (2) are supported.</span></span> <span data-ttu-id="523cc-118">Vea [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="523cc-118">See [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="523cc-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="523cc-119">Return value</span></span>

<span data-ttu-id="523cc-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="523cc-120">This method can return one of these values.</span></span>



| <span data-ttu-id="523cc-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="523cc-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="523cc-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="523cc-122">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="523cc-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-123"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="523cc-124">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="523cc-124">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="523cc-125"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="523cc-126">El parámetro *imagePath* es **null**.</span><span class="sxs-lookup"><span data-stu-id="523cc-126">The *imagePath* parameter is **NULL**.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="523cc-127"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="523cc-128">El parámetro *imageType* no es [**vmFloppyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) o **vmFloppyDiskImage \_ HighDensity** (2).</span><span class="sxs-lookup"><span data-stu-id="523cc-128">The *imageType* parameter is not [**vmFloppyDiskImage\_LowDensity**](vmfloppydiskimagetype.md) (1) or **vmFloppyDiskImage\_HighDensity** (2).</span></span><br/> |
| <dl> <span data-ttu-id="523cc-129"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="523cc-130">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="523cc-130">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="523cc-131"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="523cc-132">El parámetro *imagePath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="523cc-132">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                           |
| <dl> <span data-ttu-id="523cc-133"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="523cc-134">El parámetro *imagePath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="523cc-134">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="523cc-135">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="523cc-135">An absolute path is required.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="523cc-136"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="523cc-137">La ruta de acceso especificada por el parámetro *imagePath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="523cc-137">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="523cc-138">La longitud de la ruta de acceso debe ser inferior a 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="523cc-138">The length of the path must be less than 260 characters.</span></span><br/>                          |
| <dl> <span data-ttu-id="523cc-139"><dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="523cc-140">El archivo al que hace referencia el parámetro *imagePath* ya existe.</span><span class="sxs-lookup"><span data-stu-id="523cc-140">The file referenced by the parameter *imagePath* already exists.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="523cc-141"><dt>**HRESULT \_ DE \_ Win32 (error de \_ disco \_ lleno)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="523cc-142">No hay suficiente espacio en el volumen del host para crear la imagen de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="523cc-142">There is insufficient space on the host volume to create the virtual floppy disk image.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="523cc-143"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-143"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="523cc-144">Se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="523cc-144">An unexpected error occurred.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="523cc-145"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-145"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="523cc-146">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="523cc-146">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                           |



 

## <a name="requirements"></a><span data-ttu-id="523cc-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="523cc-147">Requirements</span></span>



| <span data-ttu-id="523cc-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="523cc-148">Requirement</span></span> | <span data-ttu-id="523cc-149">Value</span><span class="sxs-lookup"><span data-stu-id="523cc-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="523cc-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="523cc-150">Minimum supported client</span></span><br/> | <span data-ttu-id="523cc-151">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="523cc-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="523cc-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="523cc-152">Minimum supported server</span></span><br/> | <span data-ttu-id="523cc-153">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="523cc-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="523cc-154">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="523cc-154">End of client support</span></span><br/>    | <span data-ttu-id="523cc-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="523cc-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="523cc-156">Producto</span><span class="sxs-lookup"><span data-stu-id="523cc-156">Product</span></span><br/>                  | <span data-ttu-id="523cc-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="523cc-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="523cc-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="523cc-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="523cc-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="523cc-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="523cc-160">IID</span><span class="sxs-lookup"><span data-stu-id="523cc-160">IID</span></span><br/>                      | <span data-ttu-id="523cc-161">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="523cc-161">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="523cc-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="523cc-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523cc-163">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="523cc-163">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

