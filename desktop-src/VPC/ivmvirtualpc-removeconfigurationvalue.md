---
title: Método IVMVirtualPC RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Quita el valor de la opción de configuración especificada.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- Método RemoveConfigurationValue Virtual PC
- Método RemoveConfigurationValue Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905484"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a><span data-ttu-id="f545c-106">IVMVirtualPC:: RemoveConfigurationValue (método)</span><span class="sxs-lookup"><span data-stu-id="f545c-106">IVMVirtualPC::RemoveConfigurationValue method</span></span>

<span data-ttu-id="f545c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f545c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f545c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f545c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f545c-109">Quita el valor de la opción de configuración especificada.</span><span class="sxs-lookup"><span data-stu-id="f545c-109">Removes the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="f545c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f545c-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a><span data-ttu-id="f545c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f545c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f545c-112">*preferenceKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f545c-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f545c-113">Clave que se usa para identificar la preferencia, tal como se almacena en el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="f545c-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f545c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f545c-114">Return value</span></span>

<span data-ttu-id="f545c-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f545c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f545c-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f545c-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="f545c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f545c-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f545c-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f545c-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="f545c-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f545c-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f545c-120"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f545c-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="f545c-121">El parámetro *preferenceKey* es **null**.</span><span class="sxs-lookup"><span data-stu-id="f545c-121">The *preferenceKey* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f545c-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="f545c-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="f545c-123">El parámetro *preferenceKey* no es válido o es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="f545c-123">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="f545c-124"><dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="f545c-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl>                   | <span data-ttu-id="f545c-125">No se encontró la preferencia.</span><span class="sxs-lookup"><span data-stu-id="f545c-125">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f545c-126"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f545c-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="f545c-127">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="f545c-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="f545c-128"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f545c-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="f545c-129">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="f545c-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="f545c-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f545c-130">Remarks</span></span>

<span data-ttu-id="f545c-131">Este método proporciona acceso de bajo nivel a cualquier valor de preferencia para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="f545c-131">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="f545c-132">Se puede usar para quitar los valores de preferencia de las claves definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="f545c-132">It can be used to remove preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="f545c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f545c-133">Requirements</span></span>



| <span data-ttu-id="f545c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f545c-134">Requirement</span></span> | <span data-ttu-id="f545c-135">Value</span><span class="sxs-lookup"><span data-stu-id="f545c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f545c-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f545c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f545c-137">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f545c-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f545c-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f545c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f545c-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f545c-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f545c-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f545c-140">End of client support</span></span><br/>    | <span data-ttu-id="f545c-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f545c-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f545c-142">Producto</span><span class="sxs-lookup"><span data-stu-id="f545c-142">Product</span></span><br/>                  | <span data-ttu-id="f545c-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f545c-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f545c-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f545c-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f545c-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f545c-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f545c-146">IID</span><span class="sxs-lookup"><span data-stu-id="f545c-146">IID</span></span><br/>                      | <span data-ttu-id="f545c-147">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f545c-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f545c-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="f545c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f545c-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="f545c-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

