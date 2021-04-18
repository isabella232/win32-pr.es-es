---
description: La función DeletePrinterDriver quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Función DeletePrinterDriver (winspool. h)
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
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667105"
---
# <a name="deleteprinterdriver-function"></a>DeletePrinterDriver función)

La función **DeletePrinterDriver** quita el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos en un servidor.

Para eliminar los archivos asociados al controlador además de quitar el nombre del controlador de impresora especificado de la lista de nombres de los controladores admitidos para un servidor, utilice la función [**DeletePrinterDriverEx**](deleteprinterdriverex.md) .

**DeletePrinterDriver** elimina un controlador solo si no se está usando ninguna versión del controlador para el entorno especificado. [**DeletePrinterDriverEx**](deleteprinterdriverex.md) puede eliminar versiones específicas del controlador.

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

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor desde el que se va a eliminar el controlador. Si este parámetro es **null**, el nombre del controlador de impresora se quitará de forma local.

</dd> <dt>

*pEnvironment* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el entorno desde el que se va a eliminar el controlador (por ejemplo, Windows x86, Windows IA64 o Windows x64). Si este parámetro es **null**, el nombre del controlador se elimina del entorno actual de la aplicación que realiza la llamada y del equipo cliente (no de la aplicación de destino y del servidor de impresión).

</dd> <dt>

*pDriverName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del controlador que se debe eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

La función **DeletePrinterDriver** no elimina los archivos asociados, simplemente quita el nombre del controlador de la lista devuelta por la función [**EnumPrinterDrivers**](enumprinterdrivers.md) .

Antes de llamar a **DeletePrinterDriver**, debe eliminar todos los objetos de impresora que utilizan el controlador de impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

 

