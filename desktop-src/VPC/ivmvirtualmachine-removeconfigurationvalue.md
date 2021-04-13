---
title: Método IVMVirtualMachine RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Quita el valor de la configuración especificada para esta máquina virtual.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- Método RemoveConfigurationValue Virtual PC
- Método RemoveConfigurationValue Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491878"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a><span data-ttu-id="1cb07-106">IVMVirtualMachine:: RemoveConfigurationValue (método)</span><span class="sxs-lookup"><span data-stu-id="1cb07-106">IVMVirtualMachine::RemoveConfigurationValue method</span></span>

<span data-ttu-id="1cb07-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1cb07-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1cb07-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1cb07-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1cb07-109">Quita el valor de la configuración especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cb07-109">Removes the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb07-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cb07-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a><span data-ttu-id="1cb07-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cb07-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cb07-112">*configurationKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cb07-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cb07-113">Clave que se usa para identificar el valor de configuración tal y como se almacena en el \* archivo ". VMC".</span><span class="sxs-lookup"><span data-stu-id="1cb07-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cb07-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cb07-114">Return value</span></span>

<span data-ttu-id="1cb07-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1cb07-115">This method can return one of these values.</span></span>



| <span data-ttu-id="1cb07-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cb07-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="1cb07-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cb07-117">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="1cb07-118"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1cb07-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="1cb07-119">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1cb07-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="1cb07-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="1cb07-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="1cb07-121">El parámetro es **null** o está vacío.</span><span class="sxs-lookup"><span data-stu-id="1cb07-121">The parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="1cb07-122"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1cb07-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="1cb07-123">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="1cb07-123">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="1cb07-124"><dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="1cb07-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="1cb07-125">No se encontró la preferencia.</span><span class="sxs-lookup"><span data-stu-id="1cb07-125">The preference was not found.</span></span><br/>       |
| <dl> <span data-ttu-id="1cb07-126"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1cb07-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="1cb07-127">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="1cb07-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="1cb07-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cb07-128">Remarks</span></span>

<span data-ttu-id="1cb07-129">Este método proporciona acceso de bajo nivel a cualquier valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="1cb07-129">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="1cb07-130">Se puede usar para quitar los valores de configuración de las claves definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="1cb07-130">It can be used to remove configuration values for customer-defined keys.</span></span> <span data-ttu-id="1cb07-131">Tenga cuidado si usa este método para quitar los valores de configuración del sistema, ya que algunos valores no se pueden cambiar mientras se ejecuta la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cb07-131">Be careful if you use this method to remove system configuration values, since some values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="1cb07-132">Las claves de configuración se encuentran en el archivo " \* . VMC" de la máquina virtual en formato XML.</span><span class="sxs-lookup"><span data-stu-id="1cb07-132">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="1cb07-133">Las claves se almacenan de forma jerárquica, similar a las claves del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="1cb07-133">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="1cb07-134">Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="1cb07-134">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="1cb07-135">Por ejemplo, para quitar el valor de la clave "RAM \_ size" que se encuentra en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="1cb07-135">For example, to remove the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="1cb07-136">La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1cb07-136">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="1cb07-137">Si alguna de las claves del árbol deseado tiene un valor de atributo "ID", el atributo y su valor se incrustan en la cadena de ruta de acceso *configurationKey* inmediatamente después de la clave de configuración asociada con el siguiente formato entre corchetes: " \[ @id ="*ID \_* \] . "".</span><span class="sxs-lookup"><span data-stu-id="1cb07-137">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="1cb07-138">Por ejemplo, para quitar el valor de la clave "Absolute" que se encuentra en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="1cb07-138">For example, to remove the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="1cb07-139">La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1cb07-139">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="1cb07-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cb07-140">Requirements</span></span>



| <span data-ttu-id="1cb07-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cb07-141">Requirement</span></span> | <span data-ttu-id="1cb07-142">Value</span><span class="sxs-lookup"><span data-stu-id="1cb07-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb07-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cb07-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1cb07-144">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cb07-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1cb07-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cb07-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1cb07-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1cb07-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1cb07-147">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="1cb07-147">End of client support</span></span><br/>    | <span data-ttu-id="1cb07-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1cb07-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1cb07-149">Producto</span><span class="sxs-lookup"><span data-stu-id="1cb07-149">Product</span></span><br/>                  | <span data-ttu-id="1cb07-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1cb07-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1cb07-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cb07-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cb07-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cb07-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1cb07-153">IID</span><span class="sxs-lookup"><span data-stu-id="1cb07-153">IID</span></span><br/>                      | <span data-ttu-id="1cb07-154">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="1cb07-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1cb07-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cb07-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb07-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="1cb07-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

