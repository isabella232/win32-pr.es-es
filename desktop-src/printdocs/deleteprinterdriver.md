---
description: La función DeletePrinterDriver quita el nombre del controlador de impresora especificado de la lista de nombres de controladores admitidos en un servidor.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Función DeletePrinterDriver (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d878bb848eebed7eaccd904d4cdfd035d5056ee32eaa67eac5064dd5cf4e1e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060035"
---
# <a name="deleteprinterdriver-function"></a>Función DeletePrinterDriver

La **función DeletePrinterDriver** quita el nombre del controlador de impresora especificado de la lista de nombres de controladores admitidos en un servidor.

Para eliminar los archivos asociados al controlador, además de quitar el nombre de controlador de impresora especificado de la lista de nombres de controladores admitidos para un servidor, use la [**función DeletePrinterDriverEx.**](deleteprinterdriverex.md)

**DeletePrinterDriver elimina** un controlador solo si no hay ninguna versión del controlador en uso para el entorno especificado. [**DeletePrinterDriverEx puede**](deleteprinterdriverex.md) eliminar versiones específicas del controlador.

## <a name="syntax"></a>Sintaxis


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor del que se va a eliminar el controlador. Si este parámetro es **NULL,** el nombre del controlador de impresora se quitará localmente.

</dd> <dt>

*pEnvironment* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el entorno del que se va a eliminar el controlador (por ejemplo, Windows x86, Windows IA64 o Windows x64). Si este parámetro es **NULL**, el nombre del controlador se elimina del entorno actual de la aplicación que realiza la llamada y del equipo cliente (no de la aplicación de destino ni del servidor de impresión).

</dd> <dt>

*pDriverName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del controlador que se debe eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

El autor de la llamada debe [tener SeLoadDriverPrivilege.](/windows/desktop/SecAuthZ/authorization-constants)

La **función DeletePrinterDriver** no elimina los archivos asociados, simplemente quita el nombre del controlador de la lista devuelta por la función [**EnumPrinterDrivers.**](enumprinterdrivers.md)

Antes de **llamar a DeletePrinterDriver,** debe eliminar todos los objetos de impresora que usan el controlador de impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **DeletePrinterDriverW** (Unicode) y **DeletePrinterDriverA** (ANSI)<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> </dl>

 

