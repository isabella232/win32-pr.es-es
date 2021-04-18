---
description: La función SetDefaultPrinter establece el nombre de la impresora predeterminada para el usuario actual en el equipo local.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Función SetDefaultPrinter (winspool. h)
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
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716482"
---
# <a name="setdefaultprinter-function"></a>SetDefaultPrinter función)

La función **SetDefaultPrinter** establece el nombre de la impresora predeterminada para el usuario actual en el equipo local.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszPrinter* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre de impresora predeterminado. Para una conexión de impresora remota, el formato de nombre es nombredeimpresora de **\\\\** _servidor_ *_\\_* . En el caso de una impresora local, el formato de nombre es *nombreimpresora*.

Si este parámetro es **null** o una cadena vacía, es decir, "", **SetDefaultPrinter** seleccionará una impresora predeterminada de una de las impresoras instaladas. Si ya existe una impresora predeterminada, la llamada a **SetDefaultPrinter** con un **valor null** o una cadena vacía en este parámetro podría cambiar la impresora predeterminada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Al utilizar este método, debe especificar una impresora, un controlador y un puerto válidos. Si no son válidas, no se produce ningún error en las API, pero no se define el resultado. Esto puede hacer que otros programas vuelvan a establecer la impresora en la impresora válida anterior. Puede usar [**EnumPrinters**](enumprinters.md) para recuperar el nombre de la impresora, el nombre del controlador y el nombre del puerto de todas las impresoras disponibles.

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

 

 




