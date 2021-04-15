---
title: Método IVMVirtualPC CreateVirtualMachine (VPCCOMInterfaces. h)
description: Crea una nueva configuración de máquina virtual y recupera el objeto de máquina virtual.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- Método CreateVirtualMachine Virtual PC
- Método CreateVirtualMachine Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método CreateVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492046"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a>IVMVirtualPC:: CreateVirtualMachine (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Crea una nueva configuración de máquina virtual y recupera el objeto de máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configurationName* \[ de\]
</dt> <dd>

Nombre de la máquina virtual que se va a crear. La longitud del nombre no puede superar los 80 caracteres y la longitud combinada del nombre y la ruta de acceso a los archivos VMC y VMCX no pueden superar los caracteres de la **\_ ruta de acceso máxima** (260). Las extensiones de nombre de archivo. VMC y. vmcx se anexarán al final del nombre de la máquina virtual cuando se creen los archivos de configuración. Si este parámetro es **null** o una cadena vacía, el parámetro *configurationPath* debe especificar la ruta de acceso completa al archivo VMC.

</dd> <dt>

*configurationPath* \[ de\]
</dt> <dd>

La ruta de acceso a la carpeta que contendrá el archivo VMC. Esta carpeta se creará si no existe. Si *configurationName* es **null** o una cadena vacía, debe especificar la ruta de acceso completa del nuevo archivo de configuración.

</dd> <dt>

*virtualMachine* \[ out, retval\]
</dt> <dd>

Un puntero a un nuevo objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa esta máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                                                                                       |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro *configurationName* o *configurationPath* no es válido o el parámetro *virtualMachine* es **null**.<br/>                                                                               |
| <dl> <dt>**HRESULT \_ DE \_ Win32 ( \_ \_ no \_ se encontró la ruta de acceso de error)**</dt> <dt>0x80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el parámetro *configurationPath* .<br/>                                                                                                                     |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt> </dl>    | El parámetro *configurationPath* contiene un carácter no válido (uno de " \* ?: <>/ \| " ").<br/>                                                                                                        |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt> </dl>    | El parámetro *configurationPath* especifica una ruta de acceso relativa o vacía. Se requiere una ruta de acceso absoluta.<br/>                                                                                                |
| <dl> <dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por los parámetros *configurationName* y *configurationPath* da como resultado una ruta de acceso demasiado larga. La longitud total de la ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt> </dl>  | Ya existe un archivo de configuración con este nombre en esta ubicación.<br/>                                                                                                                                |
| <dl> <dt>**Máquina virtual \_ E \_ configuración \_ sin \_ nombre**</dt> <dt>0xA0040400</dt> </dl>                       | El parámetro *configurationName* está vacío.<br/>                                                                                                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ nombre de configuración \_ \_ demasiado \_ largo**</dt> <dt>0xA0040401</dt> </dl>                | El parámetro *configurationName* supera los 80 caracteres de longitud.<br/>                                                                                                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ nombre de configuración de 0xA0040402 \_ \_ \_ Char no válido**</dt> <dt></dt> </dl>            | El parámetro *configurationName* contiene un carácter no válido (uno de " \* ?: <>/ \| \\ " ").<br/>                                                                                                      |
| <dl> <dt>**Máquina virtual \_ E \_ configuración \_ \_ nombre duplicado**</dt> <dt>0xA0040403</dt> </dl>                | Ya hay una máquina virtual con este nombre.<br/>                                                                                                                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/>                                                                                                                |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

Los nombres de las máquinas virtuales no distinguen mayúsculas de minúsculas, por ejemplo, "MyVM" y "MyVM" hacen referencia a la misma máquina virtual.

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
</dt> </dl>

 

