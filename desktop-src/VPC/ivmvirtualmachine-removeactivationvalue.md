---
title: Método IVMVirtualMachine RemoveActivationValue (VPCCOMInterfaces. h)
description: Quita el valor de la configuración de activación especificada para esta máquina virtual.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- Método RemoveActivationValue Virtual PC
- Método RemoveActivationValue Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método RemoveActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079465"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a>IVMVirtualMachine:: RemoveActivationValue (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Quita el valor de la configuración de activación especificada para esta máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*activación* \[ de\]
</dt> <dd>

Clave que se usa para identificar el valor de activación tal y como se almacena en el \* archivo ". VMC".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                      | Descripción                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | El parámetro es **null** o está vacío.<br/>                                          |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>      | La configuración es desconocida.<br/>                                                |
| <dl> <dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt> </dl> | No se encontró la preferencia o esta configuración no tiene ninguna activación válida.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

Este método proporciona acceso de bajo nivel a cualquier valor de activación. Se puede usar para quitar los valores de activación de las claves definidas por el cliente. Tenga cuidado si usa este método para quitar los valores de activación del sistema, ya que algunos valores no se pueden cambiar mientras se ejecuta la máquina virtual. Cuando se inicia una máquina virtual, se realiza una copia de sus valores de configuración, que se convierte en su conjunto de valores de activación. Los valores de activación se mantienen hasta que la máquina virtual se apaga o se reinicia. Tenga en cuenta que Windows Virtual PC solo puede usar la configuración para almacenar valores para ciertas claves, es decir, el valor de activación no se puede usar nunca.

> [!Note]  
> La sesión de máquina virtual debe ejecutarse antes de que se puedan cambiar los valores de activación.

 

Las claves de activación se almacenan internamente de forma jerárquica, similar a las claves del registro de Windows. Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.

Por ejemplo, para quitar el valor de la clave " \_ acción predeterminada" que se encuentra en el siguiente árbol de claves:

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

 

