---
title: Método IVMVirtualMachine GetConfigurationValue (VPCCOMInterfaces. h)
description: Recupera el valor de la configuración especificada para esta máquina virtual.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- Método GetConfigurationValue Virtual PC
- Método GetConfigurationValue Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e98e37bd4bd5ec4ba9843ae2fdb33874a4303f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422383"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a><span data-ttu-id="30fab-106">IVMVirtualMachine:: GetConfigurationValue (método)</span><span class="sxs-lookup"><span data-stu-id="30fab-106">IVMVirtualMachine::GetConfigurationValue method</span></span>

<span data-ttu-id="30fab-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="30fab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="30fab-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="30fab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="30fab-109">Recupera el valor de la configuración especificada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="30fab-109">Retrieves the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="30fab-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30fab-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="30fab-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30fab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30fab-112">*configurationKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30fab-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30fab-113">Clave que se usa para identificar el valor de configuración tal y como se almacena en el \* archivo ". VMC".</span><span class="sxs-lookup"><span data-stu-id="30fab-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="30fab-114">*configurationValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="30fab-114">*configurationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="30fab-115">El valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="30fab-115">The configuration value.</span></span> <span data-ttu-id="30fab-116">Este valor puede ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ I4** (integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="30fab-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30fab-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30fab-117">Return value</span></span>

<span data-ttu-id="30fab-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="30fab-118">This method can return one of these values.</span></span>



| <span data-ttu-id="30fab-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30fab-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="30fab-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="30fab-120">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="30fab-121"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30fab-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="30fab-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="30fab-122">The operation was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="30fab-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="30fab-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="30fab-124">El parámetro *configurationKey* es **null** o está vacío.</span><span class="sxs-lookup"><span data-stu-id="30fab-124">The *configurationKey* parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="30fab-125"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="30fab-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="30fab-126">El parámetro *configurationValue* es **null**.</span><span class="sxs-lookup"><span data-stu-id="30fab-126">The *configurationValue* parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="30fab-127"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="30fab-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="30fab-128">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="30fab-128">The configuration is unknown.</span></span><br/>                          |
| <dl> <span data-ttu-id="30fab-129"><dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="30fab-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="30fab-130">No se encontró la preferencia.</span><span class="sxs-lookup"><span data-stu-id="30fab-130">The preference was not found.</span></span><br/>                          |
| <dl> <span data-ttu-id="30fab-131"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="30fab-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="30fab-132">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="30fab-132">An unexpected error has occurred.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="30fab-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30fab-133">Remarks</span></span>

<span data-ttu-id="30fab-134">Este método proporciona acceso de bajo nivel a cualquier valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="30fab-134">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="30fab-135">Se puede usar para leer los valores de configuración de las claves definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="30fab-135">It can be used to read configuration values for customer-defined keys.</span></span>

<span data-ttu-id="30fab-136">Las claves de configuración se encuentran en el archivo " \* . VMC" de la máquina virtual en formato XML.</span><span class="sxs-lookup"><span data-stu-id="30fab-136">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="30fab-137">Las claves se almacenan de forma jerárquica, similar a las claves del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="30fab-137">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="30fab-138">Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="30fab-138">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="30fab-139">Por ejemplo, para leer el valor de la clave "RAM \_ size" que se encuentra en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="30fab-139">For example, to read the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="30fab-140">La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="30fab-140">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="30fab-141">Si alguna de las claves del árbol deseado tiene un valor de atributo "ID", el atributo y su valor se incrustan en la cadena de ruta de acceso *configurationKey* inmediatamente después de la clave de configuración asociada con el siguiente formato entre corchetes: " \[ @id ="*ID \_* \] . "".</span><span class="sxs-lookup"><span data-stu-id="30fab-141">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="30fab-142">Por ejemplo, para leer el valor de la clave "Absolute" que se encuentra en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="30fab-142">For example, to read the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="30fab-143">La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="30fab-143">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="30fab-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30fab-144">Requirements</span></span>



| <span data-ttu-id="30fab-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="30fab-145">Requirement</span></span> | <span data-ttu-id="30fab-146">Value</span><span class="sxs-lookup"><span data-stu-id="30fab-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="30fab-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30fab-147">Minimum supported client</span></span><br/> | <span data-ttu-id="30fab-148">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="30fab-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30fab-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30fab-149">Minimum supported server</span></span><br/> | <span data-ttu-id="30fab-150">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="30fab-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="30fab-151">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="30fab-151">End of client support</span></span><br/>    | <span data-ttu-id="30fab-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30fab-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="30fab-153">Producto</span><span class="sxs-lookup"><span data-stu-id="30fab-153">Product</span></span><br/>                  | <span data-ttu-id="30fab-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="30fab-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="30fab-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30fab-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="30fab-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="30fab-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="30fab-157">IID</span><span class="sxs-lookup"><span data-stu-id="30fab-157">IID</span></span><br/>                      | <span data-ttu-id="30fab-158">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="30fab-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="30fab-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="30fab-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30fab-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="30fab-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

