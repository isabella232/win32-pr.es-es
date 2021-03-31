---
title: Método IVMVirtualPC GetFloppyDiskImageType (VPCCOMInterfaces. h)
description: Recupera el tipo de un archivo de imagen de disquete existente.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- Método GetFloppyDiskImageType Virtual PC
- Método GetFloppyDiskImageType Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método GetFloppyDiskImageType
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151073"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a><span data-ttu-id="1788f-106">IVMVirtualPC:: GetFloppyDiskImageType (método)</span><span class="sxs-lookup"><span data-stu-id="1788f-106">IVMVirtualPC::GetFloppyDiskImageType method</span></span>

<span data-ttu-id="1788f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1788f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1788f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1788f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1788f-109">Recupera el tipo de un archivo de imagen de disquete existente.</span><span class="sxs-lookup"><span data-stu-id="1788f-109">Retrieves the type of an existing floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1788f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1788f-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a><span data-ttu-id="1788f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1788f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1788f-112">*imagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1788f-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1788f-113">Ruta de acceso completa al archivo de imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="1788f-113">The full path to the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="1788f-114">*imageType* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1788f-114">*imageType* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1788f-115">El tipo de imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="1788f-115">The disk image type.</span></span> <span data-ttu-id="1788f-116">Para obtener una lista de valores, vea [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="1788f-116">For a list of values, see [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1788f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1788f-117">Return value</span></span>

<span data-ttu-id="1788f-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1788f-118">This method can return one of these values.</span></span>



| <span data-ttu-id="1788f-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1788f-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="1788f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1788f-120">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1788f-121"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="1788f-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1788f-122">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="1788f-123"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="1788f-124">El parámetro *imagePath* o *imageType* es **null**.</span><span class="sxs-lookup"><span data-stu-id="1788f-124">The *imagePath* or *imageType* parameter is **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="1788f-125"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="1788f-126">El sistema no encuentra el archivo especificado por el parámetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="1788f-126">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1788f-127"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="1788f-128">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="1788f-128">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1788f-129"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="1788f-130">El parámetro *imagePath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="1788f-130">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="1788f-131"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="1788f-132">El parámetro *imagePath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="1788f-132">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="1788f-133">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="1788f-133">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="1788f-134"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="1788f-135">La ruta de acceso especificada por el parámetro *imagePath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="1788f-135">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="1788f-136">La longitud de la ruta de acceso debe ser inferior a 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1788f-136">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="1788f-137"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="1788f-138">El archivo especificado por *imagePath* no es una imagen de disquete o se ha producido un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="1788f-138">The file specified by *imagePath* is not a floppy image, or an unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="1788f-139"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-139"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="1788f-140">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="1788f-140">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="1788f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1788f-141">Requirements</span></span>



| <span data-ttu-id="1788f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="1788f-142">Requirement</span></span> | <span data-ttu-id="1788f-143">Value</span><span class="sxs-lookup"><span data-stu-id="1788f-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1788f-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1788f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1788f-145">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1788f-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1788f-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1788f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1788f-147">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1788f-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1788f-148">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1788f-148">End of client support</span></span><br/>    | <span data-ttu-id="1788f-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1788f-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1788f-150">Producto</span><span class="sxs-lookup"><span data-stu-id="1788f-150">Product</span></span><br/>                  | <span data-ttu-id="1788f-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1788f-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1788f-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1788f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="1788f-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1788f-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1788f-154">IID</span><span class="sxs-lookup"><span data-stu-id="1788f-154">IID</span></span><br/>                      | <span data-ttu-id="1788f-155">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="1788f-155">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="1788f-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="1788f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1788f-157">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="1788f-157">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

