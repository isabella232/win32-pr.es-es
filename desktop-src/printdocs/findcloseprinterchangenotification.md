---
description: La función FindClosePrinterChangeNotification cierra un objeto de notificación de cambios creado llamando a la función FindFirstPrinterChangeNotification.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: Función FindClosePrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8040944d5890aa521681827bef786201a35da039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082604"
---
# <a name="findcloseprinterchangenotification-function"></a>FindClosePrinterChangeNotification función)

La función **FindClosePrinterChangeNotification** cierra un objeto de notificación de cambios creado llamando a la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . Dicho objeto ya no supervisará la impresora o el servidor de impresión asociado al objeto de notificación de cambios.

## <a name="syntax"></a>Sintaxis


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hChange* \[ de\]
</dt> <dd>

Identificador del objeto de notificación de cambio que se va a cerrar. Se trata de un identificador creado mediante una llamada a la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Después de llamar a la función **FindClosePrinterChangeNotification** , no se puede usar el identificador *hChange* en llamadas posteriores a [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) o [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

 




