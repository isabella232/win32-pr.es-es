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
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>IVMVirtualPC:: SetConfigurationValue (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Establece el valor de la opción de configuración especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*preferenceKey* \[ de\]
</dt> <dd>

La clave que se usa para identificar las preferencias, tal como se almacena en el archivo de configuración por usuario (Options.xml en "% LocalAppData% \\ Microsoft \\ Windows Virtual PC").

> [!IMPORTANT]
> Se deben realizar cambios en Options.xml solo mediante el método **SetConfigurationValue** . No se admite el cambio de Options.xml con ningún otro método.

 

</dd> <dt>

*preferenceValue* \[ de\]
</dt> <dd>

Valor de preferencia. Este valor puede ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ UI4** (integer) o **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                | El parámetro *preferenceKey* o *preferenceValue* es **null**.<br/>                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | El parámetro *preferenceKey* no es válido o es una cadena vacía.<br/>                    |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                           | El usuario actual no tiene acceso suficiente al archivo de configuración.<br/>                  |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl> | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/> |



 

## <a name="remarks"></a>Observaciones

Se admiten los valores siguientes para el parámetro *preferenceKey* .



| valor *preferenceKey*      | Descripción                                                                                                                                                                           | Tipo de datos            | Valor predeterminado   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| "tiempo de espera de inactividad \_ "<br/> | Número de segundos que vpc.exe debe esperar antes de salir si no hay ninguna VM o aplicación activa que use las [interfaces de Windows Virtual PC](virtual-pc-interfaces.md).<br/> | entero<br/> | "30"<br/> |



 

Este método proporciona acceso de bajo nivel a cualquier valor de configuración. Se puede usar para establecer los valores de configuración de las claves definidas por el cliente. Tenga cuidado si usa este método para establecer los valores de configuración del sistema, ya que no se realiza ninguna comprobación de errores en el valor de configuración. Además, algunos valores de configuración no se pueden cambiar mientras se ejecuta una máquina virtual.

Las claves de configuración se encuentran en el archivo "Options.xml" de la máquina virtual en formato XML. Las claves se almacenan de forma jerárquica, similar a las claves del registro de Windows. Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.

Por ejemplo, para establecer el valor de la clave "tiempo de espera de inactividad" que se \_ encuentra en el siguiente árbol de claves:

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

La cadena de ruta de acceso *preferenceKey* se especificaría de la siguiente manera:

``` syntax
"idle_timeout"
```

Si alguna de las claves del árbol deseado tiene un valor de atributo "ID", el atributo y su valor se incrustan en la cadena de ruta de acceso *preferenceKey* inmediatamente después de la clave de configuración asociada con el siguiente formato entre corchetes: " \[ @id ="*ID \_* \] . "".

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

La cadena de ruta de acceso *preferenceKey* se especificaría de la siguiente manera:

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
| IID<br/>                      | IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> <dt>

[**IVMVirtualMachine::SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

