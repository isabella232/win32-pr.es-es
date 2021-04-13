---
title: Método IVMVirtualPC GetVirtualMachineFiles (VPCCOMInterfaces. h)
description: Recupera una matriz de archivos de configuración de máquina virtual conocidos.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- Método GetVirtualMachineFiles Virtual PC
- Método GetVirtualMachineFiles Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método GetVirtualMachineFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359843"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a><span data-ttu-id="dfa1b-106">IVMVirtualPC:: GetVirtualMachineFiles (método)</span><span class="sxs-lookup"><span data-stu-id="dfa1b-106">IVMVirtualPC::GetVirtualMachineFiles method</span></span>

<span data-ttu-id="dfa1b-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dfa1b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dfa1b-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dfa1b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dfa1b-109">Recupera una matriz de archivos de configuración de máquina virtual conocidos.</span><span class="sxs-lookup"><span data-stu-id="dfa1b-109">Retrieves an array of known virtual machine configuration files.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa1b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfa1b-110">Syntax</span></span>


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a><span data-ttu-id="dfa1b-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfa1b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa1b-112">*inAdditionalSearchPaths* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dfa1b-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa1b-113">Estas rutas de acceso se buscarán junto con las rutas de acceso establecidas en las propiedades [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) y [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) .</span><span class="sxs-lookup"><span data-stu-id="dfa1b-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="dfa1b-114">*inExcludedRegisteredVMs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dfa1b-114">*inExcludedRegisteredVMs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa1b-115">**True** si las máquinas virtuales registradas se deben excluir de la devolución de la matriz en el parámetro *outVirtualMachineFileList* y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dfa1b-115">**TRUE** if registered virtual machines should be excluded from the array return in the *outVirtualMachineFileList* parameter and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="dfa1b-116">*outVirtualMachineFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="dfa1b-116">*outVirtualMachineFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa1b-117">Matriz de cadenas de ruta de acceso para los archivos de configuración de la máquina virtual que se encuentran en las rutas de búsqueda especificadas.</span><span class="sxs-lookup"><span data-stu-id="dfa1b-117">An array of path strings for the virtual machine configuration files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa1b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfa1b-118">Return value</span></span>

<span data-ttu-id="dfa1b-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="dfa1b-119">This method can return one of these values.</span></span>



| <span data-ttu-id="dfa1b-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfa1b-120">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="dfa1b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfa1b-121">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfa1b-122"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dfa1b-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="dfa1b-123">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dfa1b-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="dfa1b-124"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="dfa1b-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="dfa1b-125">El parámetro *outVirtualMachineFileList* es **null**.</span><span class="sxs-lookup"><span data-stu-id="dfa1b-125">The *outVirtualMachineFileList* parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="dfa1b-126"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="dfa1b-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="dfa1b-127">El parámetro *inAdditionalSearchPaths* no es una matriz de cadenas.</span><span class="sxs-lookup"><span data-stu-id="dfa1b-127">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="dfa1b-128"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dfa1b-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="dfa1b-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="dfa1b-129">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="dfa1b-130"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="dfa1b-130"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="dfa1b-131">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="dfa1b-131">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfa1b-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfa1b-132">Remarks</span></span>

<span data-ttu-id="dfa1b-133">Las rutas de acceso de búsqueda usadas para recuperar la matriz de archivos de configuración incluirán los establecidos anteriormente por [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) y [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) , además de los especificados por el parámetro *inAdditionalSearchPaths* .</span><span class="sxs-lookup"><span data-stu-id="dfa1b-133">The search paths used to retrieve the array of configuration files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa1b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfa1b-134">Requirements</span></span>



| <span data-ttu-id="dfa1b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfa1b-135">Requirement</span></span> | <span data-ttu-id="dfa1b-136">Value</span><span class="sxs-lookup"><span data-stu-id="dfa1b-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa1b-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfa1b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa1b-138">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="dfa1b-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dfa1b-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfa1b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa1b-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dfa1b-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dfa1b-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="dfa1b-141">End of client support</span></span><br/>    | <span data-ttu-id="dfa1b-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa1b-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dfa1b-143">Producto</span><span class="sxs-lookup"><span data-stu-id="dfa1b-143">Product</span></span><br/>                  | <span data-ttu-id="dfa1b-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dfa1b-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dfa1b-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfa1b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfa1b-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa1b-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dfa1b-147">IID</span><span class="sxs-lookup"><span data-stu-id="dfa1b-147">IID</span></span><br/>                      | <span data-ttu-id="dfa1b-148">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="dfa1b-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="dfa1b-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfa1b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa1b-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="dfa1b-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

