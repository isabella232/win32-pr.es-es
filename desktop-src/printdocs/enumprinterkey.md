---
description: La función EnumPrinterKey enumera las subclaves de una clave especificada para una impresora especificada.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Función EnumPrinterKey (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c3666cce36884a331085d074df44e05b5bcfd0422433ce24bdbf3dbc385d7f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471789"
---
# <a name="enumprinterkey-function"></a>Función EnumPrinterKey

La **función EnumPrinterKey** enumera las subclaves de una clave especificada para una impresora especificada.

Los datos de impresora se almacenan en el Registro. Al enumerar los datos de la impresora, no llame a funciones del Registro que puedan cambiar los datos.

## <a name="syntax"></a>Sintaxis


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora para la que la función enumera las subclaves. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pKeyName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la clave que contiene las subclaves que se deben enumerar. Use el carácter de barra diagonal inversa ' ' como delimitador para especificar una ruta de \\ acceso con una o varias subclaves. **EnumPrinterKey** enumera todas las subclaves de la clave, pero no enumera las subclaves de esas subclaves.

Si *pKeyName* es una cadena vacía (""), **EnumPrinterKey** enumera la clave de nivel superior de la impresora. Si *pKeyName* es **NULL,** **EnumPrinterKey** devuelve ERROR \_ INVALID \_ PARAMETER.

</dd> <dt>

*pSubkey* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de nombres de subclave terminadas en NULL. La matriz termina con dos caracteres NULL.

</dd> <dt>

*cbSubkey* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pSubkey.* Si establece *cbSubkey* en cero, el *parámetro lcSubkey* devuelve el tamaño de búfer necesario.

</dd> <dt>

*pwSubkey* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes recuperados en el *búfer pSubkey.* Si el tamaño de búfer especificado por *cbSubkey* es demasiado pequeño, la función devuelve ERROR MORE DATA y \_ \_ *lcSubkey* indica el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error del sistema. Si *pKeyName no* existe, el valor devuelto es ERROR \_ FILE NOT \_ \_ FOUND.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumPrinterKeyW** (Unicode) y **EnumPrinterKeyA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




