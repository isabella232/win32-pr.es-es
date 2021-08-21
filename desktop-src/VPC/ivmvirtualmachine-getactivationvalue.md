---
title: Método IVMVirtualMachine GetActivationValue (VPCCOMInterfaces.h)
description: Recupera el valor de la configuración de activación especificada para esta máquina virtual.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- Método GetActivationValue de Virtual PC
- Método GetActivationValue de la interfaz Virtual PC , IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , Método GetActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e03d1178df5961ba76a0ab61e74c781315cce07f32657903e5fa3e4e0a7623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123206"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a>IVMVirtualMachine::GetActivationValue (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el valor de la configuración de activación especificada para esta máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*activationKey* \[ En\]
</dt> <dd>

Clave que se usa para identificar el valor de activación tal como se almacena en el \* archivo ".vmc".

</dd> <dt>

*activationValue* \[ out, retval\]
</dt> <dd>

Valor de activación. Este valor puede ser uno de los siguientes tipos **VARIANT:** **VT \_ ARRAY** \| **VT \_ UI1** (bytes sin procesar), **VT \_ BSTR** (cadena), **VT \_ I4** (entero) o **VT \_ BOOL** (booleano).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                      | Descripción                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>                                                |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>           | El *parámetro activationKey* es **NULL o** está vacío.<br/>                          |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>              | El *parámetro activationValue* es **NULL.**<br/>                                 |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>      | La configuración es desconocida.<br/>                                                |
| <dl> <dt>**Máquina virtual \_ E \_ NO SE ENCONTRÓ \_ LA \_**</dt> <dt>0XA0040300</dt> </dl> | No se encontró la preferencia o esta configuración no tiene ninguna activación válida.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/>                                            |



 

## <a name="remarks"></a>Comentarios

Este método proporciona acceso de bajo nivel a cualquier valor de activación. Se puede usar para establecer valores de activación para claves definidas por el cliente. Cuando se inicia una máquina virtual, se realiza una copia de sus valores de configuración, que se convierten en su conjunto de valores de activación. Los valores de activación se mantienen hasta que la máquina virtual se apaga o se reinicia. Tenga en cuenta Windows Virtual PC solo puede usar la configuración para almacenar valores para determinadas claves, es decir, el valor de activación nunca se puede usar.

Las claves de activación se almacenan internamente de forma jerárquica similar a las claves del Registro de Windows. Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por marcas de barra diagonal.

Por ejemplo, para leer el valor de la clave "acción \_ predeterminada" ubicada en el siguiente árbol de claves:

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



| Requisito | Valor |
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

 

