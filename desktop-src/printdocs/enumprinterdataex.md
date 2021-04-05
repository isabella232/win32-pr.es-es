---
description: La función EnumPrinterDataEx enumera todos los nombres de valor y los datos de una impresora y una clave especificadas.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Función EnumPrinterDataEx (winspool. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815494"
---
# <a name="enumprinterdataex-function"></a>EnumPrinterDataEx función)

La función **EnumPrinterDataEx** enumera todos los nombres de valor y los datos de una impresora y una clave especificadas.

Los datos de la impresora se almacenan en el registro. Al enumerar los datos de la impresora, no llame a las funciones del registro que podrían cambiar los datos.

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora para la que la función recupera datos de configuración. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pKeyName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica la clave que contiene los valores que se van a enumerar. Use el carácter de barra diagonal inversa ( \\ ) como delimitador para especificar una ruta de acceso con una o más subclaves. **EnumPrinterDataEx** enumera todos los valores de la clave, pero no enumera los valores de las subclaves de la clave especificada. Utilice la función [**EnumPrinterKey**](enumprinterkey.md) para enumerar las subclaves.

Si *pKeyName* es **null** o una cadena vacía, **EnumPrinterDataEx** devuelve un \_ parámetro no válido \_ .

</dd> <dt>

*pEnumValues* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe una matriz de estructuras de [**\_ \_ valores de enumeración de impresora**](printer-enum-values.md) . Cada estructura contiene el nombre del valor, el tipo, los datos y los tamaños de un valor bajo la clave.

</dd> <dt>

*cbEnumValues* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pcbEnumValues*. Si establece *cbEnumValues* en cero, el parámetro *pcbEnumValues* devuelve el tamaño de búfer necesario.

</dd> <dt>

*pcbEnumValues* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño, en bytes, de los datos de configuración recuperados. Si el tamaño de búfer especificado por *cbEnumValues* es demasiado pequeño, la función devuelve un error \_ más \_ datos y *pcbEnumValues* indica el tamaño de búfer necesario.

</dd> <dt>

*pnEnumValues* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras [**de \_ \_ valores de enumeración de impresora**](printer-enum-values.md) devueltas en *pEnumValues*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error del sistema.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

**EnumPrinterDataEx** recupera los datos de configuración de la impresora establecidos por las funciones [**SetPrinterDataEx**](setprinterdataex.md) y [**SetPrinterData**](setprinterdata.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

[**\_valores de enumeración de impresora \_**](printer-enum-values.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




