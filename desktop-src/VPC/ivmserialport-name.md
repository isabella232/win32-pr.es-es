---
title: Propiedad nombre de IVMSerialPort (VPCCOMInterfaces. h)
description: Nombre del puerto serie.
ms.assetid: 4d3fe008-f089-4a1b-9c90-2e0b3ded58fa
keywords:
- Propiedad nombre virtual PC
- Propiedad nombre virtual PC, interfaz IVMSerialPort
- Interfaz IVMSerialPort Virtual PC, propiedad Name
topic_type:
- apiref
api_name:
- IVMSerialPort.Name
- IVMSerialPort.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540540e2af91647b9c77735a1c601ed62aecdbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905531"
---
# <a name="ivmserialportname-property"></a>IVMSerialPort:: Name (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el nombre del puerto serie.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre del puerto serie. Por ejemplo, "COM1" para **vmSerialPort \_ denominaba hostport**, "C: \\SerialPort.txt" para **vmSerialPort \_ TextFile** o " \\ \\ *ServerName* \\ Pipe \\ *pipename*" para **vmSerialPort \_ NamedPipe**.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>                               |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl> | La configuración de esta máquina virtual no es válida.<br/> |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort se define como 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

