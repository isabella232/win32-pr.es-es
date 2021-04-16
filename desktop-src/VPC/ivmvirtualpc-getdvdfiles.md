---
title: Método IVMVirtualPC GetDVDFiles (VPCCOMInterfaces. h)
description: Recupera una matriz de archivos de DVD conocidos.
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- Método GetDVDFiles Virtual PC
- Método GetDVDFiles Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método GetDVDFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a91d7f0d65d1f62feb21d41bd9b27bf6ce112ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695996"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a><span data-ttu-id="3ce47-106">IVMVirtualPC:: GetDVDFiles (método)</span><span class="sxs-lookup"><span data-stu-id="3ce47-106">IVMVirtualPC::GetDVDFiles method</span></span>

<span data-ttu-id="3ce47-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3ce47-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3ce47-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3ce47-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3ce47-109">Recupera una matriz de archivos de DVD conocidos.</span><span class="sxs-lookup"><span data-stu-id="3ce47-109">Retrieves an array of known DVD files.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ce47-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ce47-110">Syntax</span></span>


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a><span data-ttu-id="3ce47-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ce47-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce47-112">*inAdditionalSearchPaths* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ce47-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce47-113">Estas rutas de acceso se buscarán junto con las rutas de acceso establecidas en la propiedad [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) .</span><span class="sxs-lookup"><span data-stu-id="3ce47-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="3ce47-114">*outDVDFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3ce47-114">*outDVDFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3ce47-115">Matriz de archivos de DVD virtual que se encuentra en las rutas de acceso de búsqueda especificadas.</span><span class="sxs-lookup"><span data-stu-id="3ce47-115">An array of virtual DVD files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce47-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ce47-116">Return value</span></span>

<span data-ttu-id="3ce47-117">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3ce47-117">This method can return one of these values.</span></span>



| <span data-ttu-id="3ce47-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ce47-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="3ce47-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ce47-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ce47-120"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3ce47-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="3ce47-121">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3ce47-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3ce47-122"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3ce47-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="3ce47-123">El parámetro *outDVDFileList* es **null**.</span><span class="sxs-lookup"><span data-stu-id="3ce47-123">The *outDVDFileList* parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="3ce47-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3ce47-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="3ce47-125">El parámetro *inAdditionalSearchPaths* no es una matriz de cadenas.</span><span class="sxs-lookup"><span data-stu-id="3ce47-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="3ce47-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3ce47-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="3ce47-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="3ce47-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="3ce47-128"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="3ce47-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="3ce47-129">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="3ce47-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3ce47-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ce47-130">Remarks</span></span>

<span data-ttu-id="3ce47-131">Las rutas de acceso de búsqueda que se usan para recuperar la matriz de archivos incluirán los establecidos anteriormente por [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) además de los especificados por el parámetro *inAdditionalSearchPaths* y la ubicación del instalador para el módulo Integration Components.</span><span class="sxs-lookup"><span data-stu-id="3ce47-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter and the installer location for the integration components module.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce47-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ce47-132">Requirements</span></span>



| <span data-ttu-id="3ce47-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ce47-133">Requirement</span></span> | <span data-ttu-id="3ce47-134">Value</span><span class="sxs-lookup"><span data-stu-id="3ce47-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce47-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ce47-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce47-136">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ce47-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ce47-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ce47-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce47-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3ce47-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3ce47-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3ce47-139">End of client support</span></span><br/>    | <span data-ttu-id="3ce47-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ce47-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3ce47-141">Producto</span><span class="sxs-lookup"><span data-stu-id="3ce47-141">Product</span></span><br/>                  | <span data-ttu-id="3ce47-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3ce47-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3ce47-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ce47-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce47-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ce47-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3ce47-145">IID</span><span class="sxs-lookup"><span data-stu-id="3ce47-145">IID</span></span><br/>                      | <span data-ttu-id="3ce47-146">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="3ce47-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3ce47-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ce47-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce47-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="3ce47-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

