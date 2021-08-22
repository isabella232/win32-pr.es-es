---
title: Método IVMVirtualPC RegisterVirtualMachine (VPCCOMInterfaces.h)
description: Registra una configuración de máquina virtual existente y recupera el objeto de máquina virtual.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- RegisterVirtualMachine, método Virtual PC
- Método RegisterVirtualMachine virtual PC , interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método RegisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3752b613bb3adc97d1e0968d989b5c97c616b76883ef89880be7c00d720c62a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998544"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a>IVMVirtualPC::RegisterVirtualMachine (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Registra una configuración de máquina virtual existente y recupera el objeto de máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configurationName* \[ En\]
</dt> <dd>

Nombre de la máquina virtual que se va a registrar. La longitud del nombre no puede superar los 80 caracteres y la longitud combinada del nombre y la ruta de acceso no puede superar **los caracteres MAX \_ PATH** (260). El nombre especificado puede contener la extensión .vmc. Si este parámetro es **NULL o** una cadena vacía, el *parámetro configurationPath* debe especificar la ruta de acceso completa al archivo de configuración.

</dd> <dt>

*configurationPath* \[ En\]
</dt> <dd>

Ruta de acceso a la carpeta que contiene el archivo de configuración existente. Si el *parámetro configurationName* es **NULL o** una cadena vacía, debe especificar la ruta de acceso completa al archivo de configuración existente.

</dd> <dt>

*virtualMachine* \[ out, retval\]
</dt> <dd>

Puntero a un nuevo [**objeto IVMVirtualMachine**](ivmvirtualmachine.md) que representa esta máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                                                                                                          |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                    | El *parámetro configurationName* o *configurationPath* no es válido o *virtualMachine* es **NULL.**<br/>                                                                                                  |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (RUTA DE ACCESO DE ERROR \_ \_ NO \_ ENCONTRADA)**</dt> <dt>0X80070003</dt> </dl> | El sistema no puede encontrar la ruta de acceso especificada por los *parámetros configurationName* y *configurationPath.*<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32 (ARCHIVO DE ERROR \_ \_ NO \_ ENCONTRADO)**</dt> <dt>0X80070002</dt> </dl> | El sistema no puede encontrar el archivo especificado por los *parámetros configurationName* y *configurationPath.*<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ INVALID \_ NAME) 0X8007007B**</dt> <dt></dt> </dl>    | El *parámetro configurationPath* contiene un carácter no válido (uno de " \* ?:<>/ \| "").<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | El parámetro *configurationPath especifica* una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                                                                                         |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por los parámetros *configurationName* y *configurationPath* da como resultado una ruta de acceso demasiado larga. La longitud combinada de la ruta de acceso debe ser menor que **MAX \_ PATH** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ YA \_ EXISTE) 0X800700B7**</dt> <dt></dt> </dl>  | Ya existe un archivo de configuración con este nombre en esta ubicación.<br/>                                                                                                                                   |
| <dl> <dt>**Máquina virtual \_ E \_ CONFIG NAME TOO LONG \_ \_ \_ 0xA0040401**</dt> <dt></dt> </dl>                | El *parámetro configurationName* supera los 80 caracteres de longitud.<br/>                                                                                                                                     |
| <dl> <dt>**Máquina virtual \_ E \_ CONFIG NAME INVALID \_ \_ \_ CHAR**</dt> <dt>0xA0040402</dt> </dl>            | El *parámetro configurationName* contiene un carácter no válido (uno de " \* ?:<>/ \| \\ "").<br/>                                                                                                         |
| <dl> <dt>**Máquina virtual \_ E \_ CONFIG DUPLICATE NAME \_ \_ 0xA0040403**</dt> <dt></dt> </dl>                | Ya hay una máquina virtual con este nombre.<br/>                                                                                                                                                     |
| <dl> <dt>**Máquina virtual \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl>     | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/>                                                                                                                   |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentarios

Los nombres de máquina virtual no tienen en cuenta mayúsculas de minúsculas, por ejemplo, "MyVM" y "myvm" hacen referencia a la misma máquina virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

