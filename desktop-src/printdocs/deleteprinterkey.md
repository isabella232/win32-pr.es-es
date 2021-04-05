---
description: La función DeletePrinterKey elimina una clave especificada y todas sus subclaves para una impresora especificada.
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: Función DeletePrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815355"
---
# <a name="deleteprinterkey-function"></a>DeletePrinterKey función)

La función **DeletePrinterKey** elimina una clave especificada y todas sus subclaves para una impresora especificada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora para la que la función elimina una clave. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pKeyName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica la clave que se va a eliminar. Use el carácter de barra diagonal inversa ( \\ ) como delimitador para especificar una ruta de acceso con una o más subclaves.

Si *pKeyName* es una cadena vacía (""), **DeletePrinterKey** elimina todas las claves por debajo de la clave de nivel superior de la impresora. Si *pKeyName* es **null**, **DELETEPRINTERKEY** devuelve un \_ parámetro de error no válido \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error del sistema.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **DeletePrinterKeyW** (Unicode) y **DeletePrinterKeyA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
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

 

 




