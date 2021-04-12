---
title: Método IVMVirtualPC SetConfigurationValue (VPCCOMInterfaces. h)
description: Establece el valor de la opción de configuración especificada.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Método SetConfigurationValue Virtual PC
- Método SetConfigurationValue Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534852"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a><span data-ttu-id="16009-106">IVMVirtualPC:: SetConfigurationValue (método)</span><span class="sxs-lookup"><span data-stu-id="16009-106">IVMVirtualPC::SetConfigurationValue method</span></span>

<span data-ttu-id="16009-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="16009-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="16009-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="16009-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="16009-109">Establece el valor de la opción de configuración especificada.</span><span class="sxs-lookup"><span data-stu-id="16009-109">Sets the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="16009-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16009-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="16009-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16009-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16009-112">*preferenceKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="16009-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16009-113">La clave que se usa para identificar las preferencias, tal como se almacena en el archivo de configuración por usuario (Options.xml en "% LocalAppData% \\ Microsoft \\ Windows Virtual PC").</span><span class="sxs-lookup"><span data-stu-id="16009-113">The key used to identify the preference, as stored in the per-user configuration file (Options.xml in "%LocalAppData%\\Microsoft\\Windows Virtual PC").</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16009-114">Se deben realizar cambios en Options.xml solo mediante el método **SetConfigurationValue** .</span><span class="sxs-lookup"><span data-stu-id="16009-114">Changes should be made to Options.xml only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="16009-115">No se admite el cambio de Options.xml con ningún otro método.</span><span class="sxs-lookup"><span data-stu-id="16009-115">Changing Options.xml using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="16009-116">*preferenceValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="16009-116">*preferenceValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16009-117">Valor de preferencia.</span><span class="sxs-lookup"><span data-stu-id="16009-117">The preference value.</span></span> <span data-ttu-id="16009-118">Este valor puede ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ UI4** (integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="16009-118">This value may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16009-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16009-119">Return value</span></span>

<span data-ttu-id="16009-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="16009-120">This method can return one of these values.</span></span>



| <span data-ttu-id="16009-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16009-121">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="16009-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="16009-122">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16009-123"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="16009-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="16009-124">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="16009-124">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="16009-125"><dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="16009-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="16009-126">El parámetro *preferenceKey* o *preferenceValue* es **null**.</span><span class="sxs-lookup"><span data-stu-id="16009-126">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="16009-127"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="16009-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="16009-128">El parámetro *preferenceKey* no es válido o es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="16009-128">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="16009-129"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="16009-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="16009-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="16009-130">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="16009-131"><dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="16009-131"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                           | <span data-ttu-id="16009-132">El usuario actual no tiene acceso suficiente al archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="16009-132">The current user has insufficient access to the configuration file.</span></span><br/>                  |
| <dl> <span data-ttu-id="16009-133"><dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="16009-133"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="16009-134">El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).</span><span class="sxs-lookup"><span data-stu-id="16009-134">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16009-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16009-135">Remarks</span></span>

<span data-ttu-id="16009-136">Se admiten los valores siguientes para el parámetro *preferenceKey* .</span><span class="sxs-lookup"><span data-stu-id="16009-136">The following values are supported for the *preferenceKey* parameter.</span></span>



| <span data-ttu-id="16009-137">valor *preferenceKey*</span><span class="sxs-lookup"><span data-stu-id="16009-137">*preferenceKey* value</span></span>      | <span data-ttu-id="16009-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="16009-138">Description</span></span>                                                                                                                                                                           | <span data-ttu-id="16009-139">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="16009-139">Data type</span></span>            | <span data-ttu-id="16009-140">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="16009-140">Default value</span></span>   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| <span data-ttu-id="16009-141">"tiempo de espera de inactividad \_ "</span><span class="sxs-lookup"><span data-stu-id="16009-141">"idle\_timeout"</span></span><br/> | <span data-ttu-id="16009-142">Número de segundos que vpc.exe debe esperar antes de salir si no hay ninguna VM o aplicación activa que use las [interfaces de Windows Virtual PC](virtual-pc-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="16009-142">Number of seconds that vpc.exe should wait before exiting if there are no active VMs or applications using the [Windows Virtual PC Interfaces](virtual-pc-interfaces.md).</span></span><br/> | <span data-ttu-id="16009-143">entero</span><span class="sxs-lookup"><span data-stu-id="16009-143">"integer"</span></span><br/> | <span data-ttu-id="16009-144">"30"</span><span class="sxs-lookup"><span data-stu-id="16009-144">"30"</span></span><br/> |



 

<span data-ttu-id="16009-145">Este método proporciona acceso de bajo nivel a cualquier valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="16009-145">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="16009-146">Se puede usar para establecer los valores de configuración de las claves definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="16009-146">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="16009-147">Tenga cuidado si usa este método para establecer los valores de configuración del sistema, ya que no se realiza ninguna comprobación de errores en el valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="16009-147">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="16009-148">Además, algunos valores de configuración no se pueden cambiar mientras se ejecuta una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="16009-148">Also, some configuration values cannot be changed while a virtual machine is running.</span></span>

<span data-ttu-id="16009-149">Las claves de configuración se encuentran en el archivo "Options.xml" de la máquina virtual en formato XML.</span><span class="sxs-lookup"><span data-stu-id="16009-149">Configuration keys are located in the virtual machine's "Options.xml" file in XML format.</span></span> <span data-ttu-id="16009-150">Las claves se almacenan de forma jerárquica, similar a las claves del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="16009-150">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="16009-151">Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="16009-151">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="16009-152">Por ejemplo, para establecer el valor de la clave "tiempo de espera de inactividad" que se \_ encuentra en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="16009-152">For example, to set the value of the "idle\_timeout" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

<span data-ttu-id="16009-153">La cadena de ruta de acceso *preferenceKey* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="16009-153">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"idle_timeout"
```

<span data-ttu-id="16009-154">Si alguna de las claves del árbol deseado tiene un valor de atributo "ID", el atributo y su valor se incrustan en la cadena de ruta de acceso *preferenceKey* inmediatamente después de la clave de configuración asociada con el siguiente formato entre corchetes: " \[ @id ="*ID \_* \] . "".</span><span class="sxs-lookup"><span data-stu-id="16009-154">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *preferenceKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="16009-155">Por ejemplo, para establecer el valor de la clave "Golf" ubicada en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="16009-155">For example, to set the value of the "golf" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

<span data-ttu-id="16009-156">La cadena de ruta de acceso *preferenceKey* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="16009-156">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="16009-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16009-157">Requirements</span></span>



| <span data-ttu-id="16009-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="16009-158">Requirement</span></span> | <span data-ttu-id="16009-159">Value</span><span class="sxs-lookup"><span data-stu-id="16009-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="16009-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16009-160">Minimum supported client</span></span><br/> | <span data-ttu-id="16009-161">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="16009-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16009-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16009-162">Minimum supported server</span></span><br/> | <span data-ttu-id="16009-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="16009-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="16009-164">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="16009-164">End of client support</span></span><br/>    | <span data-ttu-id="16009-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="16009-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="16009-166">Producto</span><span class="sxs-lookup"><span data-stu-id="16009-166">Product</span></span><br/>                  | <span data-ttu-id="16009-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="16009-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="16009-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16009-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="16009-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="16009-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="16009-170">IID</span><span class="sxs-lookup"><span data-stu-id="16009-170">IID</span></span><br/>                      | <span data-ttu-id="16009-171">IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="16009-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="16009-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="16009-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16009-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="16009-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> <dt>

[<span data-ttu-id="16009-174">**IVMVirtualMachine::SetConfigurationValue**</span><span class="sxs-lookup"><span data-stu-id="16009-174">**IVMVirtualMachine::SetConfigurationValue**</span></span>](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

