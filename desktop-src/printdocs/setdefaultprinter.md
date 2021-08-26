---
description: La función SetDefaultPrinter establece el nombre de impresora de la impresora predeterminada para el usuario actual en el equipo local.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Función SetDefaultPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 570e0d57c4a04cd4845883e825acfbbef0282186cc7289751737798ed52b9592
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112125"
---
# <a name="setdefaultprinter-function"></a>Función SetDefaultPrinter

La **función SetDefaultPrinter** establece el nombre de impresora de la impresora predeterminada para el usuario actual en el equipo local.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszPrinter* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre de impresora predeterminado. Para una conexión de impresora remota, el formato de nombre es **\\\\** _server_ *_\\_* _printername_. Para una impresora local, el formato de nombre es *printername*.

Si este parámetro es **NULL** o una cadena vacía, es decir, "", **SetDefaultPrinter** seleccionará una impresora predeterminada de una de las impresoras instaladas. Si ya existe una impresora predeterminada, llamar a **SetDefaultPrinter** con **un valor NULL** o una cadena vacía en este parámetro podría cambiar la impresora predeterminada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Al usar este método, debe especificar una impresora, un controlador y un puerto válidos. Si no son válidas, las API no producirán errores, pero el resultado no está definido. Esto podría hacer que otros programas vuelvan a establecer la impresora en la impresora válida anterior. Puede usar [**EnumPrinters para**](enumprinters.md) recuperar el nombre de impresora, el nombre del controlador y el nombre del puerto de todas las impresoras disponibles.

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
| Nombres Unicode y ANSI<br/>   | **SetDefaultPrinterW** (Unicode) y **SetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetDefaultPrinter**](getdefaultprinter.md)
</dt> </dl>

 

 




