---
title: Método IVMVirtualMachine GetActivationValue (VPCCOMInterfaces. h)
description: Recupera el valor de la configuración de activación especificada para esta máquina virtual.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- Método GetActivationValue Virtual PC
- Método GetActivationValue Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método GetActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b51e34feb654fa9c5ab00ed7906268cdc9ec3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359661"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a><span data-ttu-id="c4bc4-106">IVMVirtualMachine:: GetActivationValue (método)</span><span class="sxs-lookup"><span data-stu-id="c4bc4-106">IVMVirtualMachine::GetActivationValue method</span></span>

<span data-ttu-id="c4bc4-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c4bc4-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c4bc4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c4bc4-109">Recupera el valor de la configuración de activación especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-109">Retrieves the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4bc4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4bc4-110">Syntax</span></span>


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="c4bc4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4bc4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4bc4-112">*activación* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4bc4-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bc4-113">Clave que se usa para identificar el valor de activación tal y como se almacena en el \* archivo ". VMC".</span><span class="sxs-lookup"><span data-stu-id="c4bc4-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="c4bc4-114">*activationValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c4bc4-114">*activationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bc4-115">Valor de activación.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-115">The activation value.</span></span> <span data-ttu-id="c4bc4-116">Este valor puede ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ I4** (integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="c4bc4-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY** \| **VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4bc4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4bc4-117">Return value</span></span>

<span data-ttu-id="c4bc4-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-118">This method can return one of these values.</span></span>



| <span data-ttu-id="c4bc4-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4bc4-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="c4bc4-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4bc4-120">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4bc4-121"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc4-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="c4bc4-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-122">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="c4bc4-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc4-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="c4bc4-124">El parámetro *activación* es **null** o está vacío.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-124">The *activationKey* parameter is **NULL** or empty.</span></span><br/>                          |
| <dl> <span data-ttu-id="c4bc4-125"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc4-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="c4bc4-126">El parámetro *activationValue* es **null**.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-126">The *activationValue* parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c4bc4-127"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c4bc4-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="c4bc4-128">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-128">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="c4bc4-129"><dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc4-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="c4bc4-130">No se encontró la preferencia o esta configuración no tiene ninguna activación válida.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-130">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="c4bc4-131"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc4-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="c4bc4-132">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-132">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="c4bc4-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4bc4-133">Remarks</span></span>

<span data-ttu-id="c4bc4-134">Este método proporciona acceso de bajo nivel a cualquier valor de activación.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-134">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="c4bc4-135">Se puede usar para establecer los valores de activación de las claves definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-135">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="c4bc4-136">Cuando se inicia una máquina virtual, se realiza una copia de sus valores de configuración, que se convierte en su conjunto de valores de activación.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="c4bc4-137">Los valores de activación se mantienen hasta que la máquina virtual se apaga o se reinicia.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="c4bc4-138">Tenga en cuenta que Windows Virtual PC solo puede usar la configuración para almacenar valores para ciertas claves, es decir, el valor de activación no se puede usar nunca.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

<span data-ttu-id="c4bc4-139">Las claves de activación se almacenan internamente de forma jerárquica, similar a las claves del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-139">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="c4bc4-140">Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="c4bc4-140">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="c4bc4-141">Por ejemplo, para leer el valor de la clave " \_ acción predeterminada" que se encuentra en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="c4bc4-141">For example, to read the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="c4bc4-142">La cadena de ruta de acceso *activación* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c4bc4-142">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="c4bc4-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4bc4-143">Requirements</span></span>



| <span data-ttu-id="c4bc4-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4bc4-144">Requirement</span></span> | <span data-ttu-id="c4bc4-145">Value</span><span class="sxs-lookup"><span data-stu-id="c4bc4-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bc4-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4bc4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c4bc4-147">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4bc4-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4bc4-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4bc4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c4bc4-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c4bc4-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c4bc4-150">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c4bc4-150">End of client support</span></span><br/>    | <span data-ttu-id="c4bc4-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c4bc4-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c4bc4-152">Producto</span><span class="sxs-lookup"><span data-stu-id="c4bc4-152">Product</span></span><br/>                  | <span data-ttu-id="c4bc4-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c4bc4-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c4bc4-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4bc4-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4bc4-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4bc4-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c4bc4-156">IID</span><span class="sxs-lookup"><span data-stu-id="c4bc4-156">IID</span></span><br/>                      | <span data-ttu-id="c4bc4-157">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c4bc4-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c4bc4-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4bc4-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4bc4-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="c4bc4-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

