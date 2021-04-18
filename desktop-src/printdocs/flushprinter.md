---
description: La función FlushPrinter envía un búfer a la impresora para borrarlo de un estado transitorio.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Función FlushPrinter (winspool. h)
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
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545355"
---
# <a name="flushprinter-function"></a>FlushPrinter función)

La función **FlushPrinter** envía un búfer a la impresora para borrarlo de un estado transitorio.

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador del objeto Printer. Debe ser el mismo identificador que se utilizó en una llamada anterior a [**WritePrinter**](writeprinter.md) , por parte del controlador de impresora.

</dd> <dt>

*pBuf* \[ de\]
</dt> <dd>

Puntero a una matriz de bytes que contiene los datos que se van a escribir en la impresora.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, de la matriz a la que apunta *pBuf*.

</dd> <dt>

*pcWritten* \[ enuncia\]
</dt> <dd>

Un puntero a un valor que recibe el número de bytes de datos que se escribieron en la impresora.

</dd> <dt>

*cSleep* \[ de\]
</dt> <dd>

El tiempo, en milisegundos, durante el que la línea de e/s en el puerto de impresora debe mantenerse inactiva.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Solo se debe llamar a **FlushPrinter** si se produce un error de [**WritePrinter**](writeprinter.md) , lo que dejaría a la impresora en un estado transitorio. Por ejemplo, la impresora puede entrar en un estado transitorio cuando se anula el trabajo y el controlador de impresora ha enviado parcialmente algunos datos sin procesar a la impresora.

**FlushPrinter** también puede especificar un período de inactividad durante el cual el administrador de trabajos de impresión no programa ningún trabajo en el puerto de impresora correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




