---
title: Método IVMSerialPort Configure (VPCCOMInterfaces.h)
description: Configura el puerto serie.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configuración del método Virtual PC
- Configuración del método Virtual PC, interfaz IVMSerialPort
- IVMSerialPort interface Virtual PC , Configure method
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
ms.openlocfilehash: e6e67d84239f7b672b5b8c47346d1dde73de6a35c1e99a3ba231b8425fe8b7d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136628"
---
# <a name="ivmserialportconfigure-method"></a>IVMSerialPort::Configure (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*portType* \[ En\]
</dt> <dd>

Tipo de puerto serie. Para obtener una lista de valores, [**vea VMSerialPortType**](vmserialporttype.md).

</dd> <dt>

*portName* \[ En\]
</dt> <dd>

Nombre del puerto serie. Por ejemplo, "COM1" para **vmSerialPort \_ HostPort**, "C:SerialPort.txt" para \\ **vmSerialPort \_ TextFile** o " \\ \\ *servername* \\ \\ *pipename*" para **vmSerialPort \_ NamedPipe**.

</dd> <dt>

*vmConnectImmediately* \[ En\]
</dt> <dd>

**TRUE** si el puerto serie del host debe abrirse inmediatamente cuando se inicia la máquina virtual y **FALSE** en caso contrario. Se omite si *portType* no es **vmSerialPort \_ HostPort**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                                  | La operación se realizó correctamente.<br/>                                                                                          |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                                 | El *parámetro portType* no es válido.<br/>                                                                                 |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Se produjo un error inesperado.<br/>                                                                                      |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                    | El *parámetro portName* es **NULL.**<br/>                                                                                  |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | No hay suficiente memoria disponible para completar esta solicitud.<br/>                                                         |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | La ruta de acceso especificada por el *parámetro portName* es demasiado larga. La ruta de acceso debe tener menos **de MAX \_ PATH** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ NOMBRE NO \_ VÁLIDO)**</dt> <dt>0x8007007b</dt> </dl>    | El *parámetro portName* contiene un carácter no válido (uno de " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | El *parámetro portName* especifica una ruta de acceso vacía o relativa. Se requiere una ruta de acceso absoluta.<br/>                            |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | La configuración de esta máquina virtual no es válida.<br/>                                                               |
| <dl> <dt>**Máquina virtual \_ E \_ PREF \_ ILLEGAL VALUE \_ 0xA0040301**</dt> <dt></dt> </dl>                   | El puerto especificado ya está en uso.<br/>                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMSerialPort se define como \_ 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

