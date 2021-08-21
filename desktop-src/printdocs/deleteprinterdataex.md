---
description: La función DeletePrinterDataEx elimina un valor especificado de los datos de configuración de una impresora.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: Función DeletePrinterDataEx (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7a47b3a7a62ac9dd48a86a7ddf4d6634304a402b69d5dc191ce17e3f149ffb27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950075"
---
# <a name="deleteprinterdataex-function"></a>Función DeletePrinterDataEx

La **función DeletePrinterDataEx** elimina un valor especificado de los datos de configuración de una impresora. Los datos de configuración de una impresora constan de un conjunto de valores con nombre y con tipo almacenados en una jerarquía de claves del Registro. La función elimina un valor especificado bajo una clave especificada.

Al igual [**que la función DeletePrinterData,**](deleteprinterdata.md) **DeletePrinterDataEx** puede eliminar los valores almacenados por la [**función SetPrinterData.**](setprinterdata.md) Además, **DeletePrinterDataEx puede** eliminar los valores almacenados bajo una clave especificada por la [**función SetPrinterDataEx.**](setprinterdataex.md)

## <a name="syntax"></a>Sintaxis


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora para la que la función elimina un valor. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pKeyName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la clave que contiene el valor que se debe eliminar. Use el carácter de barra diagonal inversa ( ) como delimitador para especificar una ruta de \\ acceso que tenga una o varias subclaves.

Si *pKeyName es* **NULL o** una cadena vacía, **DeletePrinterDataEx** devuelve ERROR \_ INVALID \_ PARAMETER.

</dd> <dt>

*pValueName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del valor que se eliminará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error del sistema.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **DeletePrinterDataExW** (Unicode) y **DeletePrinterDataExA** (ANSI)<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterKey**](deleteprinterkey.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




