---
description: La función FlushPrinter envía un búfer a la impresora para borrarlo de un estado transitorio.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Función FlushPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 78bd5b6ccc86651a717c29db8b938508c857f83dbd3bdf5364fb1596b8a2c956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949305"
---
# <a name="flushprinter-function"></a>Función FlushPrinter

La **función FlushPrinter** envía un búfer a la impresora para borrarlo de un estado transitorio.

## <a name="syntax"></a>Sintaxis


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador del objeto de impresora. Debe ser el mismo identificador que usó el controlador de impresora en una llamada a [**WritePrinter**](writeprinter.md) anterior.

</dd> <dt>

*pBuf* \[ En\]
</dt> <dd>

Puntero a una matriz de bytes que contiene los datos que se escribirán en la impresora.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, de la matriz a la que apunta *pBuf*.

</dd> <dt>

*pcWritten* \[ out\]
</dt> <dd>

Puntero a un valor que recibe el número de bytes de datos que se escribieron en la impresora.

</dd> <dt>

*cSleep* \[ En\]
</dt> <dd>

Tiempo, en milisegundos, durante el que se debe mantener inactiva la línea de E/S al puerto de la impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Solo se debe llamar a **FlushPrinter** si se produce un error [**en WritePrinter,**](writeprinter.md) lo que deja la impresora en un estado transitorio. Por ejemplo, la impresora podría entrar en un estado transitorio cuando se anula el trabajo y el controlador de impresora ha enviado parcialmente algunos datos sin procesar a la impresora.

**FlushPrinter también** puede especificar un período de inactividad durante el cual el colador de impresión no programa ningún trabajo en el puerto de impresora correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




