---
description: La función DeletePrinter elimina el objeto de impresora especificado.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Función DeletePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697134"
---
# <a name="deleteprinter-function"></a>DeletePrinter función)

La función **DeletePrinter** elimina el objeto de impresora especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ in, out\]
</dt> <dd>

Identificador de un objeto de impresora que se va a eliminar. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Si quedan trabajos de impresión para su procesamiento en la impresora especificada, **DeletePrinter** marca la impresora para su eliminación pendiente y, a continuación, la elimina cuando se hayan impreso todos los trabajos de impresión. No se puede agregar ningún trabajo de impresión a una impresora marcada para eliminación pendiente.

No se puede mantener una impresora marcada para eliminación pendiente, pero sus trabajos de impresión se pueden mantener, reanudar y reiniciar. Si la impresora está contenida y hay trabajos para la impresora, **DeletePrinter** produce un error de \_ acceso \_ denegado.

Tenga en cuenta que **DeletePrinter** no cierra el identificador que se le ha pasado. Por lo tanto, la aplicación debe seguir llamando a [**ClosePrinter**](closeprinter.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter (**](addprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




