---
title: Método IVMVirtualMachine SetActivationValue (VPCCOMInterfaces. h)
description: Establece el valor de la configuración de activación especificada para esta máquina virtual.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- Método SetActivationValue Virtual PC
- Método SetActivationValue Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método SetActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7cb48b5691a9ca99a0fca5b696d8b545a40e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492226"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a><span data-ttu-id="8fb7a-106">IVMVirtualMachine:: SetActivationValue (método)</span><span class="sxs-lookup"><span data-stu-id="8fb7a-106">IVMVirtualMachine::SetActivationValue method</span></span>

<span data-ttu-id="8fb7a-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8fb7a-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8fb7a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8fb7a-109">Establece el valor de la configuración de activación especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-109">Sets the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb7a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fb7a-110">Syntax</span></span>


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="8fb7a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fb7a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb7a-112">*activación* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fb7a-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb7a-113">Clave que se usa para identificar el valor de activación tal y como se almacena en el \* archivo ". VMC".</span><span class="sxs-lookup"><span data-stu-id="8fb7a-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="8fb7a-114">*activationValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fb7a-114">*activationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb7a-115">Valor de activación.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-115">The activation value.</span></span> <span data-ttu-id="8fb7a-116">Este valor puede ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ UI4** (integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="8fb7a-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb7a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fb7a-117">Return value</span></span>

<span data-ttu-id="8fb7a-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-118">This method can return one of these values.</span></span>



| <span data-ttu-id="8fb7a-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fb7a-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="8fb7a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fb7a-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8fb7a-121"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8fb7a-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="8fb7a-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-122">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="8fb7a-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8fb7a-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="8fb7a-124">El parámetro *activación* es **null** o está vacío, o bien el parámetro *activationValue* no es un tipo Variant válido.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-124">The *activationKey* parameter is **NULL** or empty, or the *activationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="8fb7a-125"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8fb7a-125"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="8fb7a-126">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-126">The configuration is unknown.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="8fb7a-127"><dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="8fb7a-127"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="8fb7a-128">La configuración no tiene una activación válida.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-128">The configuration has no valid activation.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="8fb7a-129"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8fb7a-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="8fb7a-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-130">An unexpected error has occurred.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="8fb7a-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fb7a-131">Remarks</span></span>

<span data-ttu-id="8fb7a-132">Este método proporciona acceso de bajo nivel a cualquier valor de activación.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-132">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="8fb7a-133">Se puede usar para establecer los valores de activación de las claves definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-133">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="8fb7a-134">Tenga cuidado si usa este método para establecer los valores de activación del sistema, ya que no se realiza ninguna comprobación de errores en el valor de activación.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-134">Be careful if you use this method to set system activation values, since no error checking is performed on the activation value.</span></span> <span data-ttu-id="8fb7a-135">Además, algunos valores de activación no se pueden cambiar mientras se ejecuta la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-135">Also, some activation values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="8fb7a-136">Cuando se inicia una máquina virtual, se realiza una copia de sus valores de configuración, que se convierte en su conjunto de valores de activación.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="8fb7a-137">Los valores de activación se mantienen hasta que la máquina virtual se apaga o se reinicia.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="8fb7a-138">Tenga en cuenta que Windows Virtual PC solo puede usar la configuración para almacenar valores para ciertas claves, es decir, el valor de activación no se puede usar nunca.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="8fb7a-139">La sesión de máquina virtual debe ejecutarse antes de que se puedan cambiar los valores de activación.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-139">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="8fb7a-140">Las claves de activación se almacenan internamente de forma jerárquica, similar a las claves del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-140">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="8fb7a-141">Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="8fb7a-141">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="8fb7a-142">Por ejemplo, para establecer el valor de la clave " \_ acción predeterminada" que se encuentra en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="8fb7a-142">For example, to set the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="8fb7a-143">La cadena de ruta de acceso *activación* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8fb7a-143">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="8fb7a-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fb7a-144">Requirements</span></span>



| <span data-ttu-id="8fb7a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb7a-145">Requirement</span></span> | <span data-ttu-id="8fb7a-146">Value</span><span class="sxs-lookup"><span data-stu-id="8fb7a-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb7a-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fb7a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb7a-148">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fb7a-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8fb7a-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fb7a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb7a-150">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8fb7a-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8fb7a-151">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8fb7a-151">End of client support</span></span><br/>    | <span data-ttu-id="8fb7a-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8fb7a-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8fb7a-153">Producto</span><span class="sxs-lookup"><span data-stu-id="8fb7a-153">Product</span></span><br/>                  | <span data-ttu-id="8fb7a-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8fb7a-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8fb7a-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fb7a-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fb7a-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb7a-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8fb7a-157">IID</span><span class="sxs-lookup"><span data-stu-id="8fb7a-157">IID</span></span><br/>                      | <span data-ttu-id="8fb7a-158">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="8fb7a-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8fb7a-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fb7a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb7a-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="8fb7a-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

