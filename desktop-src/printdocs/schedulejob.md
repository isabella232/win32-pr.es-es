---
description: La función ScheduleJob solicita que el colador de impresión programe un trabajo de impresión especificado para la impresión.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Función ScheduleJob (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 9a09d3e67b4be422f10db7761f28a2aa873e9bd0d84ec2c09de23ae20c7cea4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470230"
---
# <a name="schedulejob-function"></a>Función ScheduleJob

La **función ScheduleJob** solicita que el colador de impresión programe un trabajo de impresión especificado para la impresión.

## <a name="syntax"></a>Sintaxis


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora para el trabajo de impresión. Debe ser una impresora local que esté configurada como una impresora en cola. Si *hPrinter es* un identificador para una conexión de impresora remota o si la impresora está configurada para impresión directa, se produce un error **en la función ScheduleJob.** Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

*hPrinter debe* ser el mismo identificador de impresora especificado en la llamada a [**AddJob**](addjob.md) que obtuvo el *identificador del trabajo de impresión dwJobID.*

</dd> <dt>

*dwJobID* \[ En\]
</dt> <dd>

Trabajo de impresión que se va a programar. Para obtener este identificador de trabajo de impresión, llame a [**la función AddJob.**](addjob.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Debe llamar correctamente a la [**función AddJob**](addjob.md) antes de llamar **a la función ScheduleJob.** **AddJob** obtiene el identificador del trabajo de impresión que se pasa **a ScheduleJob** como *dwJobID.* Ambas llamadas deben usar el mismo valor para *hPrinter.*

La **función ScheduleJob** comprueba si hay un archivo de cola válido. Si hay un archivo de cola de impresión no válido, o si está vacío, **ScheduleJob** elimina tanto el archivo de cola como la entrada del trabajo de impresión correspondiente en el cola de impresión.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




