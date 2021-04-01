---
title: Método IVMVirtualPC GetConfigurationValue (VPCCOMInterfaces. h)
description: Recupera el valor de la opción de configuración especificada.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Método GetConfigurationValue Virtual PC
- Método GetConfigurationValue Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150792"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a><span data-ttu-id="6845d-106">IVMVirtualPC:: GetConfigurationValue (método)</span><span class="sxs-lookup"><span data-stu-id="6845d-106">IVMVirtualPC::GetConfigurationValue method</span></span>

<span data-ttu-id="6845d-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6845d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6845d-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6845d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6845d-109">Recupera el valor de la opción de configuración especificada.</span><span class="sxs-lookup"><span data-stu-id="6845d-109">Retrieves the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="6845d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6845d-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="6845d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6845d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6845d-112">*preferenceKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6845d-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6845d-113">Clave que se usa para identificar la preferencia, tal como se almacena en el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="6845d-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="6845d-114">*preferenceValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6845d-114">*preferenceValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6845d-115">Valor de preferencia.</span><span class="sxs-lookup"><span data-stu-id="6845d-115">The preference value.</span></span> <span data-ttu-id="6845d-116">Este parámetro puede ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ I4** (integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="6845d-116">This parameter may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6845d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6845d-117">Return value</span></span>

<span data-ttu-id="6845d-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6845d-118">This method can return one of these values.</span></span>



| <span data-ttu-id="6845d-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6845d-119">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="6845d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="6845d-120">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6845d-121"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6845d-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="6845d-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6845d-122">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6845d-123"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6845d-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="6845d-124">El parámetro *preferenceKey* o *preferenceValue* es **null**.</span><span class="sxs-lookup"><span data-stu-id="6845d-124">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="6845d-125"><dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="6845d-125"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xa0040300</dt></span></span> </dl>                   | <span data-ttu-id="6845d-126">No se encontró la preferencia.</span><span class="sxs-lookup"><span data-stu-id="6845d-126">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6845d-127"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="6845d-127"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="6845d-128">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="6845d-128">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="6845d-129"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6845d-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="6845d-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="6845d-130">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="6845d-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6845d-131">Remarks</span></span>

<span data-ttu-id="6845d-132">Este método proporciona acceso de bajo nivel a cualquier valor de preferencia para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="6845d-132">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="6845d-133">Se puede usar para recuperar los valores de preferencia de las claves definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="6845d-133">It can be used to retrieve preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="6845d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6845d-134">Requirements</span></span>



| <span data-ttu-id="6845d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6845d-135">Requirement</span></span> | <span data-ttu-id="6845d-136">Value</span><span class="sxs-lookup"><span data-stu-id="6845d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6845d-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6845d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6845d-138">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6845d-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6845d-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6845d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6845d-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6845d-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6845d-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6845d-141">End of client support</span></span><br/>    | <span data-ttu-id="6845d-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6845d-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6845d-143">Producto</span><span class="sxs-lookup"><span data-stu-id="6845d-143">Product</span></span><br/>                  | <span data-ttu-id="6845d-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6845d-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6845d-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6845d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6845d-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6845d-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6845d-147">IID</span><span class="sxs-lookup"><span data-stu-id="6845d-147">IID</span></span><br/>                      | <span data-ttu-id="6845d-148">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="6845d-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6845d-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="6845d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6845d-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="6845d-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

