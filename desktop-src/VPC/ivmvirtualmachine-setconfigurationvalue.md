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
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a>IVMVirtualMachine:: SetConfigurationValue (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*configurationKey* \[ de\]
</dt> <dd>

Clave que se usa para identificar el valor de configuración tal y como se almacena en el \* archivo ". VMC".

> [!IMPORTANT]
> Los cambios se deben realizar en " \* . VMC" solo mediante el método **SetConfigurationValue** . No se admite el cambio de " \* . VMC" con ningún otro método.

 

</dd> <dt>

*configurationValue* \[ de\]
</dt> <dd>

El valor de configuración. Este valor Cay debe ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ UI4** (integer) o **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | El parámetro *configurationKey* es **null** o está vacío, o bien el parámetro *configurationValue* no es un tipo Variant válido.<br/> |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl> | La configuración es desconocida.<br/>                                                                                            |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                                                                        |



 

## <a name="remarks"></a>Observaciones

Se admiten los valores siguientes para el parámetro *configurationKey* .



| valor *configurationKey*                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Tipo de datos            | Valor predeterminado     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| "sincronización de hardware/BIOS/hora \_ \_ en el \_ arranque"<br/>              | "true" si el reloj CMOS de la máquina virtual se va a sincronizar con el reloj del host en el arranque; "false" en caso contrario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | booleano<br/> | "true"<br/> |
| "integración/Microsoft/sincronización de hora de host \_ \_ /habilitada" "<br/> | "true" si la sincronización de la hora del host está habilitada en los componentes de integración; "false" en caso contrario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | booleano<br/> | "true"<br/> |
| "opciones de la interfaz de usuario \_ / \_ publicación de aplicación automática \_ "<br/>                  | "true" si la publicación automática de aplicaciones está habilitada en los componentes de integración; "false" en caso contrario. También se denomina aplicaciones virtuales.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | booleano<br/> | "true"<br/> |
| " \_ Opciones de la interfaz de usuario/segundos \_ para \_ Guardar"<br/>                   | Número de segundos que hay que esperar antes de guardar la máquina virtual después de cerrar todas las aplicaciones. Sin embargo, los valores inferiores a 20 y más de 4.294.968 tienen significados especiales. Para obtener más información, consulte la lista siguiente.<br/> <dl> <dt><span id="0"></span>0,1</dt> <dd> No guarde nunca la máquina virtual.<br/> </dd> <dt><span id="120"></span>1 20</dt> <dd> Espere 20 segundos antes de guardar la máquina virtual.<br/> </dd> <dt><span id="214_294_967"></span>21 4.294.967</dt> <dd> Espere el número de segundos especificado antes de guardar la máquina virtual.<br/> </dd> <dt><span id="4_294_9684_294_967_295"></span>4.294.968 4.294.967.295</dt> <dd> Espere 4.294.968 segundos antes de guardar la máquina virtual.<br/> </dd> </dl> | entero<br/> | 300<br/>    |



 

Este método proporciona acceso de bajo nivel a cualquier valor de configuración. Se puede usar para establecer los valores de configuración de las claves definidas por el cliente. Tenga cuidado si usa este método para establecer los valores de configuración del sistema, ya que no se realiza ninguna comprobación de errores en el valor de configuración. Además, algunos valores de configuración no se pueden cambiar mientras se ejecuta la máquina virtual.

Las claves de configuración se encuentran en el archivo " \* . VMC" de la máquina virtual en formato XML. Las claves se almacenan de forma jerárquica, similar a las claves del registro de Windows. Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.

Por ejemplo, para establecer el valor de la clave "RAM \_ size" que se encuentra en el siguiente árbol de claves:

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

Si alguna de las claves del árbol deseado tiene un valor de atributo "ID", el atributo y su valor se incrustan en la cadena de ruta de acceso *configurationKey* inmediatamente después de la clave de configuración asociada con el siguiente formato entre corchetes: " \[ @id ="*ID \_* \] . "".

Por ejemplo, para establecer el valor de la clave "Golf" ubicada en el siguiente árbol de claves:

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**IVMVirtualPC::SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

