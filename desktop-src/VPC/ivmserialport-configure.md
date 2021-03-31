---
title: Método de configuración de IVMSerialPort (VPCCOMInterfaces. h)
description: Configura el puerto serie.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configurar método virtual PC
- Configurar método virtual PC, interfaz IVMSerialPort
- Interfaz IVMSerialPort Virtual PC, configurar método
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079442"
---
# <a name="ivmserialportconfigure-method"></a>IVMSerialPort:: Configure (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Configura el puerto serie.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*portType* \[ de\]
</dt> <dd>

El tipo de puerto serie. Para obtener una lista de valores, vea [**VMSerialPortType**](vmserialporttype.md).

</dd> <dt>

*portName* \[ de\]
</dt> <dd>

Nombre del puerto serie. Por ejemplo, "COM1" para **vmSerialPort \_ denominaba hostport**, "C: \\SerialPort.txt" para **vmSerialPort \_ TextFile** o " \\ \\ *ServerName* \\ Pipe \\ *pipename*" para **vmSerialPort \_ NamedPipe**.

</dd> <dt>

*vmConnectImmediately* \[ de\]
</dt> <dd>

**True** si el puerto serie del host debe abrirse inmediatamente cuando se inicia la máquina virtual y **false** en caso contrario. Se omite si *portType* no es **vmSerialPort \_ denominaba hostport**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | El parámetro *portType* no es válido.<br/>                                                                                 |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                      |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                    | El parámetro *portName* es **null**.<br/>                                                                                  |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | No hay suficiente memoria disponible para completar esta solicitud.<br/>                                                         |
| <dl> <dt>**HRESULT \_ De \_ Win32 (desbordamiento de búfer de error \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el parámetro *portName* es demasiado larga. La ruta de acceso debe ser menor que el número máximo de caracteres de **\_ ruta de acceso** (260).<br/> |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ de \_ nombre no válido)**</dt> <dt>0x8007007b</dt> </dl>    | El parámetro *portName* contiene un carácter no válido (uno de " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ nombreruta incorrecta)**</dt> <dt>0x800700a1</dt> </dl>    | El parámetro *portName* especifica una ruta de acceso relativa o vacía. Se requiere una ruta de acceso absoluta.<br/>                            |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>                            | La configuración de esta máquina virtual no es válida.<br/>                                                               |
| <dl> <dt>**Máquina virtual \_ E \_ prefe el \_ \_ valor no válido**</dt> <dt>0xA0040301</dt> </dl>                   | El puerto especificado ya está en uso.<br/>                                                                                  |



 

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

 

