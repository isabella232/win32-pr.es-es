---
title: Método IVMVirtualMachine RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Quita el valor de la configuración especificada para esta máquina virtual.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- Método RemoveConfigurationValue Virtual PC
- Método RemoveConfigurationValue Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491878"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a>IVMVirtualMachine:: RemoveConfigurationValue (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Quita el valor de la configuración especificada para esta máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configurationKey* \[ de\]
</dt> <dd>

Clave que se usa para identificar el valor de configuración tal y como se almacena en el \* archivo ". VMC".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                      | Descripción                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | El parámetro es **null** o está vacío.<br/> |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>      | La configuración es desconocida.<br/>       |
| <dl> <dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt> </dl> | No se encontró la preferencia.<br/>       |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/>   |



 

## <a name="remarks"></a>Observaciones

Este método proporciona acceso de bajo nivel a cualquier valor de configuración. Se puede usar para quitar los valores de configuración de las claves definidas por el cliente. Tenga cuidado si usa este método para quitar los valores de configuración del sistema, ya que algunos valores no se pueden cambiar mientras se ejecuta la máquina virtual.

Las claves de configuración se encuentran en el archivo " \* . VMC" de la máquina virtual en formato XML. Las claves se almacenan de forma jerárquica, similar a las claves del registro de Windows. Para especificar una subclave específica, se construye una "ruta de acceso de clave" que especifica las distintas claves en un formato delimitado por una barra diagonal.

Por ejemplo, para quitar el valor de la clave "RAM \_ size" que se encuentra en el siguiente árbol de claves:

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:

``` syntax
"hardware/memory/ram_size"
```

Si alguna de las claves del árbol deseado tiene un valor de atributo "ID", el atributo y su valor se incrustan en la cadena de ruta de acceso *configurationKey* inmediatamente después de la clave de configuración asociada con el siguiente formato entre corchetes: " \[ @id ="*ID \_* \] . "".

Por ejemplo, para quitar el valor de la clave "Absolute" que se encuentra en el siguiente árbol de claves:

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

La cadena de ruta de acceso *configurationKey* se especificaría de la siguiente manera:

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
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

 

