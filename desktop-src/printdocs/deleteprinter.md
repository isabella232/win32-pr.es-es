---
description: La función DeletePrinter elimina el objeto de impresora especificado.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Función DeletePrinter (Winspool.h)
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
ms.openlocfilehash: 08ba5a38214e2d6fb7c9a0eedef7949551b66fd275d9a00c2d09eeab12a79bf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112575"
---
# <a name="deleteprinter-function"></a>Función DeletePrinter

La **función DeletePrinter** elimina el objeto de impresora especificado.

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

Identificador de un objeto de impresora que se eliminará. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Si quedan trabajos de impresión por procesar para la impresora especificada, **DeletePrinter** marca la impresora para su eliminación pendiente y, a continuación, la elimina cuando se han impreso todos los trabajos de impresión. No se puede agregar ningún trabajo de impresión a una impresora marcada para eliminación pendiente.

No se puede realizar una impresora marcada para eliminación pendiente, pero sus trabajos de impresión se pueden retenido, reanudado y reiniciado. Si la impresora se mantiene y hay trabajos para la impresora, **DeletePrinter** produce un error de ACCESO \_ \_ DENEGADO.

Tenga en **cuenta que DeletePrinter** no cierra el identificador que se le pasa. Por lo tanto, la aplicación todavía debe llamar [**a ClosePrinter**](closeprinter.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




