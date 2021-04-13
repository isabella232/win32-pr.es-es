---
title: Método IVMVirtualPC GetHardDiskFiles (VPCCOMInterfaces. h)
description: Recupera una matriz de archivos de disco duro virtual conocidos.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- Método GetHardDiskFiles Virtual PC
- Método GetHardDiskFiles Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método GetHardDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4162ae2667d389b445f44973c89a60fafd4c772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535170"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a><span data-ttu-id="218d6-106">IVMVirtualPC:: GetHardDiskFiles (método)</span><span class="sxs-lookup"><span data-stu-id="218d6-106">IVMVirtualPC::GetHardDiskFiles method</span></span>

<span data-ttu-id="218d6-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="218d6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="218d6-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="218d6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="218d6-109">Recupera una matriz de archivos de disco duro virtual conocidos.</span><span class="sxs-lookup"><span data-stu-id="218d6-109">Retrieves an array of known virtual hard disk files.</span></span>

## <a name="syntax"></a><span data-ttu-id="218d6-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="218d6-110">Syntax</span></span>


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a><span data-ttu-id="218d6-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="218d6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="218d6-112">*inAdditionalSearchPaths* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="218d6-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218d6-113">Estas rutas de acceso se buscarán junto con las rutas de acceso establecidas en la propiedad [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) .</span><span class="sxs-lookup"><span data-stu-id="218d6-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="218d6-114">*outHardDiskFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="218d6-114">*outHardDiskFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="218d6-115">Matriz de cadenas de ruta de acceso para los archivos de disco duro virtual encontrados en las rutas de búsqueda especificadas.</span><span class="sxs-lookup"><span data-stu-id="218d6-115">An array of path strings for the virtual hard disk files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="218d6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="218d6-116">Return value</span></span>

<span data-ttu-id="218d6-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="218d6-117">This method can return one of these values.</span></span>



| <span data-ttu-id="218d6-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="218d6-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="218d6-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="218d6-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="218d6-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="218d6-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="218d6-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="218d6-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="218d6-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="218d6-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="218d6-123">El parámetro *outHardDiskFileList* es **null**.</span><span class="sxs-lookup"><span data-stu-id="218d6-123">The *outHardDiskFileList* parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="218d6-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="218d6-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="218d6-125">El parámetro *inAdditionalSearchPaths* no es una matriz de cadenas.</span><span class="sxs-lookup"><span data-stu-id="218d6-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="218d6-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="218d6-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="218d6-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="218d6-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="218d6-128"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="218d6-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="218d6-129">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="218d6-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="218d6-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="218d6-130">Remarks</span></span>

<span data-ttu-id="218d6-131">Las rutas de acceso de búsqueda que se usan para recuperar la matriz de archivos incluirán los establecidos anteriormente por [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) además de los especificados por el parámetro *inAdditionalSearchPaths* .</span><span class="sxs-lookup"><span data-stu-id="218d6-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="218d6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="218d6-132">Requirements</span></span>



| <span data-ttu-id="218d6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="218d6-133">Requirement</span></span> | <span data-ttu-id="218d6-134">Value</span><span class="sxs-lookup"><span data-stu-id="218d6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="218d6-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="218d6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="218d6-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="218d6-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="218d6-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="218d6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="218d6-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="218d6-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="218d6-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="218d6-139">End of client support</span></span><br/>    | <span data-ttu-id="218d6-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="218d6-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="218d6-141">Producto</span><span class="sxs-lookup"><span data-stu-id="218d6-141">Product</span></span><br/>                  | <span data-ttu-id="218d6-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="218d6-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="218d6-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="218d6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="218d6-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="218d6-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="218d6-145">IID</span><span class="sxs-lookup"><span data-stu-id="218d6-145">IID</span></span><br/>                      | <span data-ttu-id="218d6-146">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="218d6-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="218d6-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="218d6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="218d6-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="218d6-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

