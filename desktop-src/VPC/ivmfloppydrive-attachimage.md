---
title: Método IVMFloppyDrive AttachImage (VPCCOMInterfaces. h)
description: Adjunta una imagen de disquete en el host a la unidad de disquete de la máquina virtual.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Método AttachImage Virtual PC
- Método AttachImage Virtual PC, interfaz IVMFloppyDrive
- Interfaz IVMFloppyDrive Virtual PC, método AttachImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996243"
---
# <a name="ivmfloppydriveattachimage-method"></a><span data-ttu-id="6f0cc-106">IVMFloppyDrive:: AttachImage (método)</span><span class="sxs-lookup"><span data-stu-id="6f0cc-106">IVMFloppyDrive::AttachImage method</span></span>

<span data-ttu-id="6f0cc-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6f0cc-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6f0cc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6f0cc-109">Adjunta una imagen de disquete en el host a la unidad de disquete de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-109">Attaches a floppy media image on the host to the floppy drive of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f0cc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f0cc-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a><span data-ttu-id="6f0cc-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f0cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f0cc-112">*mediaImagePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f0cc-112">*mediaImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f0cc-113">La ruta de acceso completa a la imagen de disquete que se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-113">The full path to the floppy media image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f0cc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f0cc-114">Return value</span></span>

<span data-ttu-id="6f0cc-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-115">This method can return one of these values.</span></span>



| <span data-ttu-id="6f0cc-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f0cc-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="6f0cc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f0cc-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f0cc-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="6f0cc-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6f0cc-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="6f0cc-121">El parámetro *mediaImagePath* no es válido.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-121">The *mediaImagePath* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="6f0cc-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="6f0cc-123">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="6f0cc-124"><dt>**HRESULT \_ DE \_ Win32 (error \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="6f0cc-125">No hay suficiente memoria disponible para completar esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-125">There is not enough memory available to complete this request.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="6f0cc-126"><dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="6f0cc-127">La ruta de acceso especificada por el parámetro *mediaImagePath* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-127">The path specified by the *mediaImagePath* parameter is too long.</span></span> <span data-ttu-id="6f0cc-128">La ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).</span><span class="sxs-lookup"><span data-stu-id="6f0cc-128">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="6f0cc-129"><dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="6f0cc-130">El parámetro *mediaImagePath* contiene un carácter no válido (uno de " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="6f0cc-130">The *mediaImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="6f0cc-131"><dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="6f0cc-132">El parámetro *mediaImagePath* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-132">The *mediaImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="6f0cc-133">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-133">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="6f0cc-134"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="6f0cc-135">La configuración de esta máquina virtual no es válida o no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-135">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="6f0cc-136"><dt>**Máquina virtual \_ E \_ captura de imagen con \_ \_ error**</dt> <dt>0xA00400650</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-136"><dt>**VM\_E\_IMAGE\_CAPTURE\_FAIL**</dt> <dt>0xA00400650</dt></span></span> </dl>                  | <span data-ttu-id="6f0cc-137">No se pudo capturar el archivo de imagen especificado.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-137">The image file specified could not be captured.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="6f0cc-138"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="6f0cc-139">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="6f0cc-139">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="6f0cc-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f0cc-140">Requirements</span></span>



| <span data-ttu-id="6f0cc-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f0cc-141">Requirement</span></span> | <span data-ttu-id="6f0cc-142">Value</span><span class="sxs-lookup"><span data-stu-id="6f0cc-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f0cc-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f0cc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6f0cc-144">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f0cc-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f0cc-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f0cc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6f0cc-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6f0cc-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6f0cc-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6f0cc-147">End of client support</span></span><br/>    | <span data-ttu-id="6f0cc-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6f0cc-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6f0cc-149">Producto</span><span class="sxs-lookup"><span data-stu-id="6f0cc-149">Product</span></span><br/>                  | <span data-ttu-id="6f0cc-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6f0cc-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6f0cc-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f0cc-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f0cc-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f0cc-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6f0cc-153">IID</span><span class="sxs-lookup"><span data-stu-id="6f0cc-153">IID</span></span><br/>                      | <span data-ttu-id="6f0cc-154">IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="6f0cc-154">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6f0cc-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f0cc-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f0cc-156">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="6f0cc-156">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

