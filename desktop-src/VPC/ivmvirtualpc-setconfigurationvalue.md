---
title: Método IVMVirtualPC SetConfigurationValue (VPCCOMInterfaces.h)
description: Establece el valor de la configuración especificada.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- SetConfigurationValue, método Virtual PC
- Método SetConfigurationValue virtual PC , interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método SetConfigurationValue
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
ms.openlocfilehash: 50d3ea585182794c1e96195fdbef842bc35c86342d390dd59e7077b31d4ef9a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591708"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>IVMVirtualPC::SetConfigurationValue (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Establece el valor de la configuración especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*preferenceKey* \[ En\]
</dt> <dd>

Clave que se usa para identificar la preferencia, tal como se almacena en el archivo de configuración por usuario (Options.xml en "%LocalAppData% \\ Microsoft \\ Windows Virtual PC").

> [!IMPORTANT]
> Se deben realizar cambios en Options.xml solo mediante el **método SetConfigurationValue.** No se Options.xml cambiar el uso de cualquier otro método.

 

</dd> <dt>

*preferenceValue* \[ En\]
</dt> <dd>

Valor de preferencia. Este valor puede ser uno de los siguientes tipos **VARIANT:** **VT \_ ARRAY** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (cadena), **VT \_ UI4** (entero) o **VT \_ BOOL** (booleano).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                | El *parámetro preferenceKey* o *preferenceValue* es **NULL.**<br/>                      |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>                             | El *parámetro preferenceKey* no es válido o es una cadena vacía.<br/>                    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                           | El usuario actual no tiene acceso suficiente al archivo de configuración.<br/>                  |
| <dl> <dt>**Máquina virtual \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/> |



 

## <a name="remarks"></a>Comentarios

Se admiten los siguientes valores para el *parámetro preferenceKey.*



| *valor preferenceKey*      | Descripción                                                                                                                                                                           | Tipo de datos            | Valor predeterminado   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| "tiempo de \_ espera de inactividad"<br/> | Número de segundos que vpc.exe debe esperar antes de salir si no hay máquinas virtuales o aplicaciones activas que usen Windows [interfaces de PC virtual](virtual-pc-interfaces.md).<br/> | "integer"<br/> | "30"<br/> |



 

Este método proporciona acceso de bajo nivel a cualquier valor de configuración. Se puede usar para establecer valores de configuración para claves definidas por el cliente. Tenga cuidado si usa este método para establecer valores de configuración del sistema, ya que no se realiza ninguna comprobación de errores en el valor de configuración. Además, algunos valores de configuración no se pueden cambiar mientras se ejecuta una máquina virtual.

Las claves de configuración se encuentran en el archivo "Options.xml" de la máquina virtual en formato XML. Las claves se almacenan de forma jerárquica similar a las claves del Registro de Windows. Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por marcas de barra diagonal.

Por ejemplo, para establecer el valor de la clave "tiempo de espera de \_ inactividad" ubicada en el siguiente árbol de claves:

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

La cadena de ruta de acceso *preferenceKey* se especificaría de la siguiente manera:

``` syntax
"idle_timeout"
```

Si alguna de las claves del árbol deseado tiene un valor de atributo "id", el atributo y su valor se incrustan en la cadena de ruta de acceso *preferenceKey* inmediatamente después de su clave de configuración asociada con el siguiente formato entre corchetes: " \[ @id ="*id \_ value*" \] ".

Por ejemplo, para establecer el valor de la clave "ctrl" ubicada en el siguiente árbol de claves:

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
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> <dt>

[**IVMVirtualMachine::SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

