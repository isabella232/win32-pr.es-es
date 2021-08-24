---
title: Método IVMVirtualMachine SetConfigurationValue (VPCCOMInterfaces.h)
description: Establece el valor de la configuración especificada para esta máquina virtual (VM).
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- SetConfigurationValue, método Virtual PC
- Método SetConfigurationValue de pc virtual, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , Método SetConfigurationValue
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
ms.openlocfilehash: 7edef64484161f6151b1d2ac14fd6916a7d2a082c0c787b983019305027f4949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652975"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a>IVMVirtualMachine::SetConfigurationValue (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Establece el valor de la configuración especificada para esta máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configurationKey* \[ En\]
</dt> <dd>

Clave usada para identificar el valor de configuración como almacenado en el \* archivo ".vmc".

> [!IMPORTANT]
> Los cambios se deben realizar en \* ".vmc" solo mediante el **método SetConfigurationValue.** No se \* admite el cambio de ".vmc" con cualquier otro método.

 

</dd> <dt>

*configurationValue* \[ En\]
</dt> <dd>

El valor de configuración. Este valor debe ser uno de los siguientes tipos **VARIANT:** **VT \_ ARRAY** \| **VT \_ UI1** (bytes sin procesar), **VT \_ BSTR** (cadena), **VT \_ UI4** (entero) o **VT \_ BOOL** (booleano).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                                                                            |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>      | El *parámetro configurationKey* es **NULL** o está vacío o el *parámetro configurationValue* no es un tipo de variante válido.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | La configuración es desconocida.<br/>                                                                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                                                                        |



 

## <a name="remarks"></a>Comentarios

Se admiten los siguientes valores para el *parámetro configurationKey.*



| *valor configurationKey*                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Tipo de datos            | Valor predeterminado     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| "hardware/bios/time \_ sync \_ at \_ boot"<br/>              | "true" si el reloj CMOS de la máquina virtual se va a sincronizar con el reloj del host durante el arranque; De lo contrario, "false".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | "booleano"<br/> | "true"<br/> |
| "integration/microsoft/host \_ time \_ sync/enabled""<br/> | "true" si la sincronización de hora del host está habilitada en los componentes de integración; De lo contrario, "false".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | "booleano"<br/> | "true"<br/> |
| "ui \_ options/auto \_ app \_ publish"<br/>                  | "true" si la publicación automática de aplicaciones está habilitada en los componentes de integración; De lo contrario, "false". Esto también se denomina aplicaciones virtuales.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | "booleano"<br/> | "true"<br/> |
| "ui \_ options/seconds \_ to \_ save"<br/>                   | Número de segundos que hay que esperar antes de guardar la máquina virtual después de cerrar todas las aplicaciones. Sin embargo, los valores inferiores a 20 y más de 4 294 968 tienen significados especiales. Para más información, consulte la lista siguiente.<br/> <dl> <dt><span id="0"></span>0</dt> <dd> No guarde nunca la máquina virtual.<br/> </dd> <dt><span id="120"></span>1 20</dt> <dd> Espere 20 segundos antes de guardar la máquina virtual.<br/> </dd> <dt><span id="214_294_967"></span>21 4,294,967</dt> <dd> Espere el número de segundos especificado antes de guardar la máquina virtual.<br/> </dd> <dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt> <dd> Espere 4 294 968 segundos antes de guardar la máquina virtual.<br/> </dd> </dl> | "integer"<br/> | 300<br/>    |



 

Este método proporciona acceso de bajo nivel a cualquier valor de configuración. Se puede usar para establecer los valores de configuración de las claves definidas por el cliente. Tenga cuidado si usa este método para establecer valores de configuración del sistema, ya que no se realiza ninguna comprobación de errores en el valor de configuración. Además, algunos valores de configuración no se pueden cambiar mientras se ejecuta la máquina virtual.

Las claves de configuración se encuentran en el archivo ".vmc" de la máquina virtual \* en formato XML. Las claves se almacenan de forma jerárquica similar a las claves del Registro en Windows. Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por marcas de barra diagonal.

Por ejemplo, para establecer el valor de la clave de "tamaño de \_ ram" ubicada en el siguiente árbol de claves:

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:

``` syntax
"hardware/memory/ram_size"
```

Si alguna de las claves del árbol deseado tiene un valor de atributo "id", el atributo y su valor se incrustan en la cadena de ruta de acceso *configurationKey* inmediatamente después de su clave de configuración asociada con el siguiente formato entre corchetes: " \[ @id ="*id \_ value*" \] ".

Por ejemplo, para establecer el valor de la clave "...", que se encuentra en el siguiente árbol de claves:

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

La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**IVMVirtualPC::SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

