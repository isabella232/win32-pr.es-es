---
title: Método IVMVirtualPC CreateVirtualMachine (VPCCOMInterfaces.h)
description: Crea una nueva configuración de máquina virtual y recupera el objeto de máquina virtual.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- CreateVirtualMachine, método Virtual PC
- Método CreateVirtualMachine Para PC virtual, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método CreateVirtualMachine
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
ms.openlocfilehash: 07dc79e5b2e8513015aaa3b83582fc8b5872a8386ff7fd66b37e144296c869c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958565"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a>IVMVirtualPC::CreateVirtualMachine (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*configurationName* \[ En\]
</dt> <dd>

Nombre de la máquina virtual que se va a crear. La longitud del nombre no puede superar los 80 caracteres y la longitud combinada del nombre y la ruta de acceso a los archivos VMC y VMCX no puede superar los caracteres **MAX \_ PATH** (260). Las extensiones de nombre de archivo .vmc y .vmcx se anexarán al final del nombre de la máquina virtual cuando se crean los archivos de configuración. Si este parámetro es **NULL o** una cadena vacía, el *parámetro configurationPath* debe especificar la ruta de acceso completa al archivo VMC.

</dd> <dt>

*configurationPath* \[ En\]
</dt> <dd>

Ruta de acceso a la carpeta que contendrá el archivo VMC. Esta carpeta se creará si no existe. Si *configurationName* es **NULL o** una cadena vacía, debe especificar la ruta de acceso completa del nuevo archivo de configuración.

</dd> <dt>

*virtualMachine* \[ out, retval\]
</dt> <dd>

Puntero a un nuevo [**objeto IVMVirtualMachine**](ivmvirtualmachine.md) que representa esta máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                                                                                       |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                    | El *parámetro configurationName* o *configurationPath* no es válido o el *parámetro virtualMachine* es **NULL.**<br/>                                                                               |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)**</dt> <dt>0X80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por el *parámetro configurationPath.*<br/>                                                                                                                     |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ NOMBRE NO \_ VÁLIDO)**</dt> <dt>0x8007007b</dt> </dl>    | El *parámetro configurationPath* contiene un carácter no válido (uno de " \* ?:<>/ \| "").<br/>                                                                                                        |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | El *parámetro configurationPath* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                                                                                                |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por los parámetros *configurationName* y *configurationPath* da como resultado una ruta de acceso demasiado larga. La longitud total de la ruta de acceso debe ser inferior a **MAX \_ PATH** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ YA \_ EXISTE)**</dt> <dt>0X800700B7</dt> </dl>  | Ya existe un archivo de configuración con este nombre en esta ubicación.<br/>                                                                                                                                |
| <dl> <dt>**Máquina virtual \_ E \_ CONFIG \_ NO \_ NAME**</dt> <dt>0xA0040400</dt> </dl>                       | El *parámetro configurationName* está vacío.<br/>                                                                                                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ NOMBRE DE CONFIGURACIÓN DEMASIADO \_ \_ \_ LARGO**</dt> <dt>0xA0040401</dt> </dl>                | El *parámetro configurationName* supera los 80 caracteres de longitud.<br/>                                                                                                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ NOMBRE DE CONFIGURACIÓN CHAR \_ \_ \_ NO**</dt> VÁLIDO <dt>0xA0040402</dt> </dl>            | El *parámetro configurationName* contiene un carácter no válido (uno de " \* ?:<>/ \| \\ "").<br/>                                                                                                      |
| <dl> <dt>**Máquina virtual \_ E \_ CONFIG DUPLICATE NAME \_ \_ 0xA0040403**</dt> <dt></dt> </dl>                | Ya hay una máquina virtual con este nombre.<br/>                                                                                                                                                  |
| <dl> <dt>**Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/>                                                                                                                |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentarios

Los nombres de máquina virtual no tienen en cuenta las mayúsculas y minúsculas; por ejemplo, "MyVM" y "myvm" hacen referencia a la misma máquina virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

