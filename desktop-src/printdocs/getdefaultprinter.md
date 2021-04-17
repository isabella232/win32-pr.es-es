---
description: La función GetDefaultPrinter recupera el nombre de la impresora predeterminada del usuario actual en el equipo local.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: Función GetDefaultPrinter (winspool. h)
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
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697155"
---
# <a name="getdefaultprinter-function"></a>GetDefaultPrinter función)

La función **GetDefaultPrinter** recupera el nombre de la impresora predeterminada del usuario actual en el equipo local.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszBuffer* \[ de\]
</dt> <dd>

Un puntero a un búfer que recibe una cadena de caracteres terminada en null que contiene el nombre de impresora predeterminado. Si este parámetro es **null**, se produce un error en la función y la variable a la que apunta *pcchBuffer* devuelve el tamaño de búfer necesario, en caracteres.

</dd> <dt>

*pcchBuffer* \[ in, out\]
</dt> <dd>

En la entrada, especifica el tamaño, en caracteres, del búfer de *pszBuffer* . En la salida, recibe el tamaño, en caracteres, de la cadena del nombre de la impresora, incluido el carácter nulo de terminación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero y la variable a la que apunta *pcchBuffer* contiene el número de caracteres copiados en el búfer *pszBuffer* , incluido el carácter nulo de terminación.

Si la función no se realiza correctamente, el valor devuelto es cero.



| Value                       | Significado                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| ERROR \_ de \_ búfer insuficiente | El búfer de *pszBuffer* es demasiado pequeño. La variable a la que apunta *pcchBuffer* contiene el tamaño de búfer necesario, en caracteres. |
| \_ \_ no \_ se encontró el archivo de error     | No hay ninguna impresora predeterminada.                                                                                                   |



 

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
| Nombres Unicode y ANSI<br/>   | **GetDefaultPrinterW** (Unicode) y **GetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**SetDefaultPrinter**](setdefaultprinter.md)
</dt> </dl>

 

 




