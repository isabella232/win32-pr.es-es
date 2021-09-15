---
description: La función EnumPrinterDataEx enumera todos los nombres de valor y los datos de una impresora y clave especificadas.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Función EnumPrinterDataEx (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468526"
---
# <a name="enumprinterdataex-function"></a>Función EnumPrinterDataEx

La **función EnumPrinterDataEx** enumera todos los nombres de valor y los datos de una impresora y clave especificadas.

Los datos de impresora se almacenan en el registro. Al enumerar los datos de la impresora, no llame a funciones del Registro que puedan cambiar los datos.

## <a name="syntax"></a>Sintaxis


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora para la que la función recupera los datos de configuración. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pKeyName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la clave que contiene los valores que se deben enumerar. Use el carácter de barra diagonal inversa ( ) como delimitador para especificar una ruta de \\ acceso con una o varias subclaves. **EnumPrinterDataEx** enumera todos los valores de la clave, pero no enumera los valores de las subclaves de la clave especificada. Use la [**función EnumPrinterKey**](enumprinterkey.md) para enumerar las subclaves.

Si *pKeyName* es **NULL o** una cadena vacía, **EnumPrinterDataEx** devuelve ERROR \_ INVALID \_ PARAMETER.

</dd> <dt>

*pEnumValues* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de estructuras [**PRINTER \_ ENUM \_ VALUES.**](printer-enum-values.md) Cada estructura contiene el nombre del valor, el tipo, los datos y los tamaños de un valor bajo la clave.

</dd> <dt>

*cbEnumValues* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *byteEnumValues.* Si establece *cbEnumValues en* cero, el parámetro *pwEnumValues* devuelve el tamaño de búfer necesario.

</dd> <dt>

*pwEnumValues* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño, en bytes, de los datos de configuración recuperados. Si el tamaño de búfer especificado por *cbEnumValues* es demasiado pequeño, la función devuelve ERROR MORE DATA y \_ \_ *pwEnumValues* indica el tamaño de búfer necesario.

</dd> <dt>

*pnEnumValues* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras [**PRINTER \_ ENUM \_ VALUES**](printer-enum-values.md) *devueltas en pEnumValues*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error del sistema.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

**EnumPrinterDataEx** recupera los datos de configuración de impresora establecidos por las funciones [**SetPrinterDataEx**](setprinterdataex.md) [**y SetPrinterData.**](setprinterdata.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumPrinterDataExW** (Unicode) y **EnumPrinterDataExA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**VALORES \_ DE ENUMERACIÓN DE \_ IMPRESORA**](printer-enum-values.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




