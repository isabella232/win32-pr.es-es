---
title: Método IVMVirtualMachine RemoveActivationValue (VPCCOMInterfaces. h)
description: Quita el valor de la configuración de activación especificada para esta máquina virtual.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- Método RemoveActivationValue Virtual PC
- Método RemoveActivationValue Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método RemoveActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079465"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a><span data-ttu-id="8da13-106">IVMVirtualMachine:: RemoveActivationValue (método)</span><span class="sxs-lookup"><span data-stu-id="8da13-106">IVMVirtualMachine::RemoveActivationValue method</span></span>

<span data-ttu-id="8da13-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8da13-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8da13-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8da13-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8da13-109">Quita el valor de la configuración de activación especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8da13-109">Removes the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da13-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8da13-110">Syntax</span></span>


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a><span data-ttu-id="8da13-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8da13-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da13-112">*activación* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8da13-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da13-113">Clave que se usa para identificar el valor de activación tal y como se almacena en el \* archivo ". VMC".</span><span class="sxs-lookup"><span data-stu-id="8da13-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8da13-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8da13-114">Return value</span></span>

<span data-ttu-id="8da13-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8da13-115">This method can return one of these values.</span></span>



| <span data-ttu-id="8da13-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8da13-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="8da13-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8da13-117">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8da13-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8da13-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="8da13-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8da13-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="8da13-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8da13-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="8da13-121">El parámetro es **null** o está vacío.</span><span class="sxs-lookup"><span data-stu-id="8da13-121">The parameter is **NULL** or empty.</span></span><br/>                                          |
| <dl> <span data-ttu-id="8da13-122"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8da13-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="8da13-123">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="8da13-123">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="8da13-124"><dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="8da13-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="8da13-125">No se encontró la preferencia o esta configuración no tiene ninguna activación válida.</span><span class="sxs-lookup"><span data-stu-id="8da13-125">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="8da13-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8da13-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="8da13-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="8da13-127">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="8da13-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8da13-128">Remarks</span></span>

<span data-ttu-id="8da13-129">Este método proporciona acceso de bajo nivel a cualquier valor de activación.</span><span class="sxs-lookup"><span data-stu-id="8da13-129">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="8da13-130">Se puede usar para quitar los valores de activación de las claves definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="8da13-130">It can be used to remove activation values for customer-defined keys.</span></span> <span data-ttu-id="8da13-131">Tenga cuidado si usa este método para quitar los valores de activación del sistema, ya que algunos valores no se pueden cambiar mientras se ejecuta la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8da13-131">Be careful if you use this method to remove system activation values, since some values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="8da13-132">Cuando se inicia una máquina virtual, se realiza una copia de sus valores de configuración, que se convierte en su conjunto de valores de activación.</span><span class="sxs-lookup"><span data-stu-id="8da13-132">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="8da13-133">Los valores de activación se mantienen hasta que la máquina virtual se apaga o se reinicia.</span><span class="sxs-lookup"><span data-stu-id="8da13-133">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="8da13-134">Tenga en cuenta que Windows Virtual PC solo puede usar la configuración para almacenar valores para ciertas claves, es decir, el valor de activación no se puede usar nunca.</span><span class="sxs-lookup"><span data-stu-id="8da13-134">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="8da13-135">La sesión de máquina virtual debe ejecutarse antes de que se puedan cambiar los valores de activación.</span><span class="sxs-lookup"><span data-stu-id="8da13-135">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="8da13-136">Las claves de activación se almacenan internamente de forma jerárquica, similar a las claves del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="8da13-136">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="8da13-137">Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="8da13-137">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="8da13-138">Por ejemplo, para quitar el valor de la clave " \_ acción predeterminada" que se encuentra en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="8da13-138">For example, to remove the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="8da13-139">La cadena de ruta de acceso *activación* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8da13-139">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="8da13-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8da13-140">Requirements</span></span>



| <span data-ttu-id="8da13-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da13-141">Requirement</span></span> | <span data-ttu-id="8da13-142">Value</span><span class="sxs-lookup"><span data-stu-id="8da13-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8da13-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8da13-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8da13-144">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8da13-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8da13-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8da13-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8da13-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8da13-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8da13-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8da13-147">End of client support</span></span><br/>    | <span data-ttu-id="8da13-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8da13-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8da13-149">Producto</span><span class="sxs-lookup"><span data-stu-id="8da13-149">Product</span></span><br/>                  | <span data-ttu-id="8da13-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8da13-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8da13-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8da13-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="8da13-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8da13-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8da13-153">IID</span><span class="sxs-lookup"><span data-stu-id="8da13-153">IID</span></span><br/>                      | <span data-ttu-id="8da13-154">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="8da13-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8da13-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="8da13-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da13-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="8da13-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

