---
title: Método IVMVirtualMachine SetActivationValue (VPCCOMInterfaces.h)
description: Establece el valor de la configuración de activación especificada para esta máquina virtual.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- SetActivationValue, método Virtual PC
- Método SetActivationValue para PC virtual, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , método SetActivationValue
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
ms.openlocfilehash: a3f7c669db848a668d294e509ad65a56ef19aebd53d0c718f12e524cfc16a940
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124725"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a>IVMVirtualMachine::SetActivationValue (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Establece el valor de la configuración de activación especificada para esta máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*activationKey* \[ En\]
</dt> <dd>

Clave usada para identificar el valor de activación como almacenado en el \* archivo ".vmc".

</dd> <dt>

*activationValue* \[ En\]
</dt> <dd>

Valor de activación. Este valor puede ser uno de los siguientes tipos **VARIANT:** **VT \_ ARRAY** \| **VT \_ UI1** (bytes sin procesar), **VT \_ BSTR** (cadena), **VT \_ UI4** (entero) o **VT \_ BOOL** (booleano).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                      | Descripción                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>                                                                                       |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>           | El *parámetro activationKey* es **NULL** o está vacío, o el parámetro *activationValue* no es un tipo de variante válido.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>      | La configuración es desconocida.<br/>                                                                                       |
| <dl> <dt>**Máquina virtual \_ E \_ PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl> | La configuración no tiene ninguna activación válida.<br/>                                                                          |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/>                                                                                   |



 

## <a name="remarks"></a>Comentarios

Este método proporciona acceso de bajo nivel a cualquier valor de activación. Se puede usar para establecer los valores de activación de las claves definidas por el cliente. Tenga cuidado si usa este método para establecer los valores de activación del sistema, ya que no se realiza ninguna comprobación de errores en el valor de activación. Además, algunos valores de activación no se pueden cambiar mientras se ejecuta la máquina virtual. Cuando se inicia una máquina virtual, se realiza una copia de sus valores de configuración, que se convierte en su conjunto de valores de activación. Los valores de activación se mantienen hasta que la máquina virtual se apaga o se reinicia. Tenga en Windows virtual solo puede usar la configuración para almacenar valores para determinadas claves, es decir, el valor de activación nunca se puede usar.

> [!Note]  
> La sesión de máquina virtual debe ejecutarse antes de que se puedan cambiar los valores de activación.

 

Las claves de activación se almacenan internamente de forma jerárquica similar a las claves del Registro de Windows. Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por marcas de barra diagonal.

Por ejemplo, para establecer el valor de la clave de "acción \_ predeterminada" ubicada en el siguiente árbol de claves:

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

La cadena de ruta de acceso *activationKey* se especificaría de la siguiente manera:

``` syntax
"settings/undo_drives/default_action"
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
</dt> </dl>

 

