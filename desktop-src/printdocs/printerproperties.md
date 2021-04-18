---
description: La función PrinterProperties muestra una hoja de propiedades de las propiedades de la impresora especificada.
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: Función PrinterProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
- winspool.drv
ms.openlocfilehash: e7e2c8586c06b2cb64a0e499bd05a6b6016de0a6
ms.sourcegitcommit: c77ed4d933c9f30af0ca0e095a75ad2bdd4d8bf8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "106011185"
---
# <a name="printerproperties-function"></a>PrinterProperties función)

La función **PrinterProperties** muestra una hoja de propiedades de las propiedades de la impresora especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Identificador de la ventana primaria de la hoja de propiedades.

</dd> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de un objeto de impresora. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

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
| Archivo DLL<br/>                      | <dl> <dt>winspool. drv</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DocumentProperties**](documentproperties.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




