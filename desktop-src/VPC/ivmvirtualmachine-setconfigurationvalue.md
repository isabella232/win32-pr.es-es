---
title: Método IVMVirtualMachine SetConfigurationValue (VPCCOMInterfaces. h)
description: Establece el valor de la configuración especificada para esta máquina virtual (VM).
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Método SetConfigurationValue Virtual PC
- Método SetConfigurationValue Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696000"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a><span data-ttu-id="6775f-106">IVMVirtualMachine:: SetConfigurationValue (método)</span><span class="sxs-lookup"><span data-stu-id="6775f-106">IVMVirtualMachine::SetConfigurationValue method</span></span>

<span data-ttu-id="6775f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6775f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6775f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6775f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6775f-109">Establece el valor de la configuración especificada para esta máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="6775f-109">Sets the value of the specified configuration setting for this virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="6775f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6775f-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="6775f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6775f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6775f-112">*configurationKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6775f-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6775f-113">Clave que se usa para identificar el valor de configuración tal y como se almacena en el \* archivo ". VMC".</span><span class="sxs-lookup"><span data-stu-id="6775f-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6775f-114">Los cambios se deben realizar en " \* . VMC" solo mediante el método **SetConfigurationValue** .</span><span class="sxs-lookup"><span data-stu-id="6775f-114">Changes should be made to "\*.vmc" only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="6775f-115">No se admite el cambio de " \* . VMC" con ningún otro método.</span><span class="sxs-lookup"><span data-stu-id="6775f-115">Changing "\*.vmc" using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="6775f-116">*configurationValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6775f-116">*configurationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6775f-117">El valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="6775f-117">The configuration value.</span></span> <span data-ttu-id="6775f-118">Este valor Cay debe ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ UI4** (integer) o **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="6775f-118">This value cay be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6775f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6775f-119">Return value</span></span>

<span data-ttu-id="6775f-120">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6775f-120">This method can return one of these values.</span></span>



| <span data-ttu-id="6775f-121">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6775f-121">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="6775f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6775f-122">Description</span></span>                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6775f-123"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6775f-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6775f-124">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6775f-124">The operation was successful.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="6775f-125"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6775f-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="6775f-126">El parámetro *configurationKey* es **null** o está vacío, o bien el parámetro *configurationValue* no es un tipo Variant válido.</span><span class="sxs-lookup"><span data-stu-id="6775f-126">The *configurationKey* parameter is **NULL** or empty or the *configurationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="6775f-127"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6775f-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6775f-128">La configuración es desconocida.</span><span class="sxs-lookup"><span data-stu-id="6775f-128">The configuration is unknown.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="6775f-129"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6775f-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6775f-130">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="6775f-130">An unexpected error has occurred.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="6775f-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6775f-131">Remarks</span></span>

<span data-ttu-id="6775f-132">Se admiten los valores siguientes para el parámetro *configurationKey* .</span><span class="sxs-lookup"><span data-stu-id="6775f-132">The following values are supported for the *configurationKey* parameter.</span></span>



| <span data-ttu-id="6775f-133">valor *configurationKey*</span><span class="sxs-lookup"><span data-stu-id="6775f-133">*configurationKey* value</span></span>                                     | <span data-ttu-id="6775f-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="6775f-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="6775f-135">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6775f-135">Data type</span></span>            | <span data-ttu-id="6775f-136">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="6775f-136">Default value</span></span>     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| <span data-ttu-id="6775f-137">"sincronización de hardware/BIOS/hora \_ \_ en el \_ arranque"</span><span class="sxs-lookup"><span data-stu-id="6775f-137">"hardware/bios/time\_sync\_at\_boot"</span></span><br/>              | <span data-ttu-id="6775f-138">"true" si el reloj CMOS de la máquina virtual se va a sincronizar con el reloj del host en el arranque; "false" en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6775f-138">"true" if the VM CMOS clock is to be synchronized with the host clock at boot; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="6775f-139">booleano</span><span class="sxs-lookup"><span data-stu-id="6775f-139">"boolean"</span></span><br/> | <span data-ttu-id="6775f-140">"true"</span><span class="sxs-lookup"><span data-stu-id="6775f-140">"true"</span></span><br/> |
| <span data-ttu-id="6775f-141">"integración/Microsoft/sincronización de hora de host \_ \_ /habilitada" "</span><span class="sxs-lookup"><span data-stu-id="6775f-141">"integration/microsoft/host\_time\_sync/enabled""</span></span><br/> | <span data-ttu-id="6775f-142">"true" si la sincronización de la hora del host está habilitada en los componentes de integración; "false" en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6775f-142">"true" if host time synchronization is enabled in the integration components; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="6775f-143">booleano</span><span class="sxs-lookup"><span data-stu-id="6775f-143">"boolean"</span></span><br/> | <span data-ttu-id="6775f-144">"true"</span><span class="sxs-lookup"><span data-stu-id="6775f-144">"true"</span></span><br/> |
| <span data-ttu-id="6775f-145">"opciones de la interfaz de usuario \_ / \_ publicación de aplicación automática \_ "</span><span class="sxs-lookup"><span data-stu-id="6775f-145">"ui\_options/auto\_app\_publish"</span></span><br/>                  | <span data-ttu-id="6775f-146">"true" si la publicación automática de aplicaciones está habilitada en los componentes de integración; "false" en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6775f-146">"true" if automatic publishing of applications is enabled in the integration components; "false" otherwise.</span></span> <span data-ttu-id="6775f-147">También se denomina aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="6775f-147">This is also called virtual applications.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="6775f-148">booleano</span><span class="sxs-lookup"><span data-stu-id="6775f-148">"boolean"</span></span><br/> | <span data-ttu-id="6775f-149">"true"</span><span class="sxs-lookup"><span data-stu-id="6775f-149">"true"</span></span><br/> |
| <span data-ttu-id="6775f-150">" \_ Opciones de la interfaz de usuario/segundos \_ para \_ Guardar"</span><span class="sxs-lookup"><span data-stu-id="6775f-150">"ui\_options/seconds\_to\_save"</span></span><br/>                   | <span data-ttu-id="6775f-151">Número de segundos que hay que esperar antes de guardar la máquina virtual después de cerrar todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6775f-151">Number of seconds to wait before saving the VM after all applications are closed.</span></span> <span data-ttu-id="6775f-152">Sin embargo, los valores inferiores a 20 y más de 4.294.968 tienen significados especiales.</span><span class="sxs-lookup"><span data-stu-id="6775f-152">However, values below 20 and more than 4,294,968 have special meanings.</span></span> <span data-ttu-id="6775f-153">Para obtener más información, consulte la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="6775f-153">For details, see the following list</span></span><br/> <dl> <span data-ttu-id="6775f-154"><dt><span id="0"></span>0,1</dt></span><span class="sxs-lookup"><span data-stu-id="6775f-154"><dt><span id="0"></span>0</dt></span></span> <dd> <span data-ttu-id="6775f-155">No guarde nunca la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6775f-155">Never save the VM.</span></span><br/> </dd> <span data-ttu-id="6775f-156"><dt><span id="120"></span>1 20</dt></span><span class="sxs-lookup"><span data-stu-id="6775f-156"><dt><span id="120"></span>1 20</dt></span></span> <dd> <span data-ttu-id="6775f-157">Espere 20 segundos antes de guardar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6775f-157">Wait 20 seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="6775f-158"><dt><span id="214_294_967"></span>21 4.294.967</dt></span><span class="sxs-lookup"><span data-stu-id="6775f-158"><dt><span id="214_294_967"></span>21 4,294,967</dt></span></span> <dd> <span data-ttu-id="6775f-159">Espere el número de segundos especificado antes de guardar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6775f-159">Wait the specified number of seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="6775f-160"><dt><span id="4_294_9684_294_967_295"></span>4.294.968 4.294.967.295</dt></span><span class="sxs-lookup"><span data-stu-id="6775f-160"><dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt></span></span> <dd> <span data-ttu-id="6775f-161">Espere 4.294.968 segundos antes de guardar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6775f-161">Wait 4,294,968 seconds before saving the VM.</span></span><br/> </dd> </dl> | <span data-ttu-id="6775f-162">entero</span><span class="sxs-lookup"><span data-stu-id="6775f-162">"integer"</span></span><br/> | <span data-ttu-id="6775f-163">300</span><span class="sxs-lookup"><span data-stu-id="6775f-163">300</span></span><br/>    |



 

<span data-ttu-id="6775f-164">Este método proporciona acceso de bajo nivel a cualquier valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="6775f-164">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="6775f-165">Se puede usar para establecer los valores de configuración de las claves definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="6775f-165">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="6775f-166">Tenga cuidado si usa este método para establecer los valores de configuración del sistema, ya que no se realiza ninguna comprobación de errores en el valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="6775f-166">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="6775f-167">Además, algunos valores de configuración no se pueden cambiar mientras se ejecuta la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6775f-167">Also, some configuration values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="6775f-168">Las claves de configuración se encuentran en el archivo " \* . VMC" de la máquina virtual en formato XML.</span><span class="sxs-lookup"><span data-stu-id="6775f-168">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="6775f-169">Las claves se almacenan de forma jerárquica, similar a las claves del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="6775f-169">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="6775f-170">Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="6775f-170">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="6775f-171">Por ejemplo, para establecer el valor de la clave "RAM \_ size" que se encuentra en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="6775f-171">For example, to set the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

<span data-ttu-id="6775f-172">La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6775f-172">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="6775f-173">Si alguna de las claves del árbol deseado tiene un valor de atributo "ID", el atributo y su valor se incrustan en la cadena de ruta de acceso *configurationKey* inmediatamente después de la clave de configuración asociada con el siguiente formato entre corchetes: " \[ @id ="*ID \_* \] . "".</span><span class="sxs-lookup"><span data-stu-id="6775f-173">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="6775f-174">Por ejemplo, para establecer el valor de la clave "Golf" ubicada en el siguiente árbol de claves:</span><span class="sxs-lookup"><span data-stu-id="6775f-174">For example, to set the value of the "golf" key located in the following key tree:</span></span>

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

<span data-ttu-id="6775f-175">La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6775f-175">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="6775f-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6775f-176">Requirements</span></span>



| <span data-ttu-id="6775f-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="6775f-177">Requirement</span></span> | <span data-ttu-id="6775f-178">Value</span><span class="sxs-lookup"><span data-stu-id="6775f-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6775f-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6775f-179">Minimum supported client</span></span><br/> | <span data-ttu-id="6775f-180">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6775f-180">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6775f-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6775f-181">Minimum supported server</span></span><br/> | <span data-ttu-id="6775f-182">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6775f-182">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6775f-183">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6775f-183">End of client support</span></span><br/>    | <span data-ttu-id="6775f-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6775f-184">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6775f-185">Producto</span><span class="sxs-lookup"><span data-stu-id="6775f-185">Product</span></span><br/>                  | <span data-ttu-id="6775f-186">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6775f-186">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6775f-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6775f-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="6775f-188"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6775f-188"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6775f-189">IID</span><span class="sxs-lookup"><span data-stu-id="6775f-189">IID</span></span><br/>                      | <span data-ttu-id="6775f-190">IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="6775f-190">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6775f-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="6775f-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6775f-192">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="6775f-192">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="6775f-193">**IVMVirtualPC::SetConfigurationValue**</span><span class="sxs-lookup"><span data-stu-id="6775f-193">**IVMVirtualPC::SetConfigurationValue**</span></span>](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

