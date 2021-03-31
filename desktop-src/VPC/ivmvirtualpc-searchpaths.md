---
title: Propiedad IVMVirtualPC SearchPaths (VPCCOMInterfaces. h)
description: Rutas de acceso del sistema de archivos que se usan para buscar archivos asociados a Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- Propiedad SearchPaths Virtual PC
- Propiedad SearchPaths Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, propiedad SearchPaths
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800961"
---
# <a name="ivmvirtualpcsearchpaths-property"></a><span data-ttu-id="7bb8d-106">IVMVirtualPC:: SearchPaths (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7bb8d-106">IVMVirtualPC::SearchPaths property</span></span>

<span data-ttu-id="7bb8d-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7bb8d-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7bb8d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7bb8d-109">Recupera y establece las rutas de acceso del sistema de archivos que se usan para buscar archivos asociados a Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-109">Retrieves and sets the file system paths that are used to find files associated with Windows Virtual PC.</span></span>

<span data-ttu-id="7bb8d-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb8d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bb8d-111">Syntax</span></span>


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a><span data-ttu-id="7bb8d-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7bb8d-112">Property value</span></span>

<span data-ttu-id="7bb8d-113">Especifica una matriz SafeArray que contiene una ruta de acceso del sistema de archivos para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-113">Specifies a safearray containing a file system path for each entry.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7bb8d-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7bb8d-114">Error codes</span></span>



| <span data-ttu-id="7bb8d-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="7bb8d-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="7bb8d-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7bb8d-116">Meaning</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7bb8d-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="7bb8d-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-118">The operation was successful.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="7bb8d-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="7bb8d-120">El parámetro es **null**.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-120">The parameter is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="7bb8d-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="7bb8d-122">El parámetro *searchPaths* no es válido y no se pudo analizar en una matriz de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-122">The *searchPaths* parameter is not valid and could not be parsed into an array of paths.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7bb8d-123"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró el archivo de error)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="7bb8d-124">El sistema no puede encontrar un directorio especificado en el parámetro *searchPaths* .</span><span class="sxs-lookup"><span data-stu-id="7bb8d-124">The system cannot find a directory specified in the *searchPaths* parameter.</span></span><br/>                                                |
| <dl> <span data-ttu-id="7bb8d-125"><dt>HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="7bb8d-126">El sistema no puede encontrar una ruta de acceso especificada por el parámetro *searchPaths* .</span><span class="sxs-lookup"><span data-stu-id="7bb8d-126">The system cannot find a path specified by the *searchPaths* parameter.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="7bb8d-127"><dt>HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-127"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="7bb8d-128">Una ruta de acceso especificada en el parámetro *searchPaths* contiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-128">A path specified in the *searchPaths* parameter contains illegal characters.</span></span> <span data-ttu-id="7bb8d-129">Los caracteres no válidos son " \* ? <>/ \| ": ".</span><span class="sxs-lookup"><span data-stu-id="7bb8d-129">The illegal characters are "\*?<>/\|":".</span></span><br/> |
| <dl> <span data-ttu-id="7bb8d-130"><dt>HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-130"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="7bb8d-131">Una ruta de acceso contenida en el parámetro *searchPaths* especifica una ruta de acceso relativa o vacía.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-131">A path contained in the *searchPaths* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="7bb8d-132">Se requiere una ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-132">An absolute path is required.</span></span><br/>          |
| <dl> <span data-ttu-id="7bb8d-133"><dt>HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-133"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="7bb8d-134">La ruta de acceso especificada en el parámetro *searchPaths* es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-134">The path specified in the *searchPaths* parameter is too long.</span></span> <span data-ttu-id="7bb8d-135">La longitud de la ruta de acceso debe ser inferior a 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-135">The length of the path must be less than 260 characters.</span></span><br/>     |
| <dl> <span data-ttu-id="7bb8d-136"><dt>Máquina virtual \_ E \_ Pref \_ not \_ found</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-136"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl>                       | <span data-ttu-id="7bb8d-137">No se encontró la preferencia.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-137">The preference was not found.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="7bb8d-138"><dt>Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-138"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="7bb8d-139">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="7bb8d-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                        |
| <dl> <span data-ttu-id="7bb8d-140"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-140"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="7bb8d-141">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="7bb8d-141">An unexpected error has occurred.</span></span><br/>                                                                                           |



## <a name="requirements"></a><span data-ttu-id="7bb8d-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bb8d-142">Requirements</span></span>



| <span data-ttu-id="7bb8d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bb8d-143">Requirement</span></span> | <span data-ttu-id="7bb8d-144">Value</span><span class="sxs-lookup"><span data-stu-id="7bb8d-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb8d-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bb8d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7bb8d-146">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7bb8d-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7bb8d-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bb8d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7bb8d-148">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7bb8d-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7bb8d-149">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7bb8d-149">End of client support</span></span><br/>    | <span data-ttu-id="7bb8d-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7bb8d-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7bb8d-151">Producto</span><span class="sxs-lookup"><span data-stu-id="7bb8d-151">Product</span></span><br/>                  | <span data-ttu-id="7bb8d-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7bb8d-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7bb8d-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bb8d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bb8d-154"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bb8d-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7bb8d-155">IID</span><span class="sxs-lookup"><span data-stu-id="7bb8d-155">IID</span></span><br/>                      | <span data-ttu-id="7bb8d-156">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="7bb8d-156">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7bb8d-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bb8d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb8d-158">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="7bb8d-158">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

