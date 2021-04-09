---
title: Método IVMVirtualPC GetHardDisk (VPCCOMInterfaces. h)
description: Recupera un objeto correspondiente a un archivo de imagen de disco existente.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- Método GetHardDisk Virtual PC
- Método GetHardDisk Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método GetHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 558d098b6745718830c63dd700c14febf4f6bed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996874"
---
# <a name="ivmvirtualpcgetharddisk-method"></a><span data-ttu-id="05570-106">IVMVirtualPC:: GetHardDisk (método)</span><span class="sxs-lookup"><span data-stu-id="05570-106">IVMVirtualPC::GetHardDisk method</span></span>

<span data-ttu-id="05570-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="05570-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="05570-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="05570-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="05570-109">Recupera un objeto correspondiente a un archivo de imagen de disco existente.</span><span class="sxs-lookup"><span data-stu-id="05570-109">Retrieves an object corresponding to an existing disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="05570-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05570-110">Syntax</span></span>


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a><span data-ttu-id="05570-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05570-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05570-112">*imagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05570-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05570-113">Ruta de acceso completa a un archivo de imagen de disco existente.</span><span class="sxs-lookup"><span data-stu-id="05570-113">The full path to an existing disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="05570-114">disco *duro* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="05570-114">*hardDisk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="05570-115">Objeto [**IVMHardDisk**](ivmharddisk.md) correspondiente a esta imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="05570-115">An [**IVMHardDisk**](ivmharddisk.md) object corresponding to this disk image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05570-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05570-116">Return value</span></span>

<span data-ttu-id="05570-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="05570-117">This method can return one of these values.</span></span>



| <span data-ttu-id="05570-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05570-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="05570-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="05570-119">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05570-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05570-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="05570-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="05570-121">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="05570-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="05570-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="05570-123">El parámetro *imagePath* o disco *duro* es **null**.</span><span class="sxs-lookup"><span data-stu-id="05570-123">The *imagePath* or *hardDisk* parameter is **NULL**.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="05570-124"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="05570-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="05570-125">El sistema no encuentra el archivo especificado por el parámetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="05570-125">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="05570-126"><dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="05570-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="05570-127">El sistema no puede encontrar la ruta de acceso especificada por el parámetro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="05570-127">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="05570-128"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="05570-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="05570-129">El parámetro *imagePath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="05570-129">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="05570-130"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="05570-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="05570-131">El parámetro *imagePath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="05570-131">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="05570-132">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="05570-132">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="05570-133"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="05570-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="05570-134">La ruta de acceso especificada por el parámetro *imagePath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="05570-134">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="05570-135">La longitud de la ruta de acceso debe ser inferior a 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="05570-135">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="05570-136"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="05570-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="05570-137">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="05570-137">An unexpected error has occurred.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="05570-138"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="05570-138"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="05570-139">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="05570-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="05570-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05570-140">Requirements</span></span>



| <span data-ttu-id="05570-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="05570-141">Requirement</span></span> | <span data-ttu-id="05570-142">Value</span><span class="sxs-lookup"><span data-stu-id="05570-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="05570-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05570-143">Minimum supported client</span></span><br/> | <span data-ttu-id="05570-144">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="05570-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05570-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05570-145">Minimum supported server</span></span><br/> | <span data-ttu-id="05570-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="05570-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="05570-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="05570-147">End of client support</span></span><br/>    | <span data-ttu-id="05570-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="05570-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="05570-149">Producto</span><span class="sxs-lookup"><span data-stu-id="05570-149">Product</span></span><br/>                  | <span data-ttu-id="05570-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05570-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="05570-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05570-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="05570-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="05570-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="05570-153">IID</span><span class="sxs-lookup"><span data-stu-id="05570-153">IID</span></span><br/>                      | <span data-ttu-id="05570-154">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="05570-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="05570-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="05570-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05570-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="05570-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

