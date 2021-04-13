---
title: Método IVMVirtualMachine SetActivationValue (VPCCOMInterfaces. h)
description: Establece el valor de la configuración de activación especificada para esta máquina virtual.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- Método SetActivationValue Virtual PC
- Método SetActivationValue Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método SetActivationValue
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
ms.openlocfilehash: 4c7cb48b5691a9ca99a0fca5b696d8b545a40e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492226"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a>IVMVirtualMachine:: SetActivationValue (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*activación* \[ de\]
</dt> <dd>

Clave que se usa para identificar el valor de activación tal y como se almacena en el \* archivo ". VMC".

</dd> <dt>

*activationValue* \[ de\]
</dt> <dd>

Valor de activación. Este valor puede ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ UI4** (integer) o **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                      | Descripción                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | El parámetro *activación* es **null** o está vacío, o bien el parámetro *activationValue* no es un tipo Variant válido.<br/> |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>      | La configuración es desconocida.<br/>                                                                                       |
| <dl> <dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt> </dl> | La configuración no tiene una activación válida.<br/>                                                                          |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/>                                                                                   |



 

## <a name="remarks"></a>Observaciones

Este método proporciona acceso de bajo nivel a cualquier valor de activación. Se puede usar para establecer los valores de activación de las claves definidas por el cliente. Tenga cuidado si usa este método para establecer los valores de activación del sistema, ya que no se realiza ninguna comprobación de errores en el valor de activación. Además, algunos valores de activación no se pueden cambiar mientras se ejecuta la máquina virtual. Cuando se inicia una máquina virtual, se realiza una copia de sus valores de configuración, que se convierte en su conjunto de valores de activación. Los valores de activación se mantienen hasta que la máquina virtual se apaga o se reinicia. Tenga en cuenta que Windows Virtual PC solo puede usar la configuración para almacenar valores para ciertas claves, es decir, el valor de activación no se puede usar nunca.

> [!Note]  
> La sesión de máquina virtual debe ejecutarse antes de que se puedan cambiar los valores de activación.

 

Las claves de activación se almacenan internamente de forma jerárquica, similar a las claves del registro de Windows. Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.

Por ejemplo, para establecer el valor de la clave " \_ acción predeterminada" que se encuentra en el siguiente árbol de claves:

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

La cadena de ruta de acceso *activación* se especificaría de la siguiente manera:

``` syntax
"settings/undo_drives/default_action"
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
</dt> </dl>

 

