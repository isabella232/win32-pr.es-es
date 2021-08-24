---
description: La función GetDefaultPrinter recupera el nombre de la impresora predeterminada para el usuario actual en el equipo local.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: Función GetDefaultPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 59d6ba435b592076455690916f5c627c73f65370df381861c25a6fafa21bf0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949105"
---
# <a name="getdefaultprinter-function"></a>Función GetDefaultPrinter

La **función GetDefaultPrinter** recupera el nombre de la impresora predeterminada para el usuario actual en el equipo local.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszBuffer* \[ En\]
</dt> <dd>

Puntero a un búfer que recibe una cadena de caracteres terminada en NULL que contiene el nombre de impresora predeterminado. Si este parámetro es **NULL,** se produce un error en la función y la variable a la que *apunta pcchBuffer* devuelve el tamaño de búfer necesario, en caracteres.

</dd> <dt>

*pcchBuffer* \[ in, out\]
</dt> <dd>

En la entrada, especifica el tamaño, en caracteres, del búfer *pszBuffer.* En la salida, recibe el tamaño, en caracteres, de la cadena de nombre de impresora, incluido el carácter nulo final.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero y la variable a la que apunta *pcchBuffer* contiene el número de caracteres copiados en el búfer *pszBuffer,* incluido el carácter nulo de terminación.

Si la función no se realiza correctamente, el valor devuelto es cero.



| Value                       | Significado                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| ERROR \_ BÚFER \_ INSUFICIENTE | El *búfer pszBuffer* es demasiado pequeño. La variable a la que apunta *pcchBuffer* contiene el tamaño de búfer necesario, en caracteres. |
| ARCHIVO \_ DE ERROR NO \_ \_ ENCONTRADO     | No hay ninguna impresora predeterminada.                                                                                                   |



 

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
| Nombres Unicode y ANSI<br/>   | **GetDefaultPrinterW** (Unicode) y **GetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**SetDefaultPrinter**](setdefaultprinter.md)
</dt> </dl>

 

 




