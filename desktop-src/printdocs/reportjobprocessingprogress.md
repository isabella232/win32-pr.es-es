---
description: Notifica al servicio de cola de impresión si un trabajo de impresión XPS está en la fase de creación de trabajos de cola o representación y qué parte del procesamiento está en curso actualmente.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Función ReportJobProcessingProgress (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a560c584568dac251ae529255958c9a26fb159631f17d1534949aba38674ccd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823995"
---
# <a name="reportjobprocessingprogress-function"></a>Función ReportJobProcessingProgress

Notifica al servicio de cola de impresión si un trabajo de impresión XPS está en la fase de creación de trabajos de cola o representación y qué parte del procesamiento está en curso actualmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*printerHandle* \[ En\]
</dt> <dd>

Identificador de impresora para el que la función va a recuperar información. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*jobId* \[ En\]
</dt> <dd>

Identifica el trabajo de impresión para el que se recuperan los datos. Use la [**función AddJob**](addjob.md) o [**startDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obtener un identificador de trabajo de impresión.

</dd> <dt>

*jobOperation* 
</dt> <dd>

Especifica si el trabajo está en la fase de cola o en la fase de representación.

</dd> <dt>

*jobProgress* 
</dt> <dd>

Especifica qué parte del procesamiento está actualmente en curso. Este valor hace referencia a eventos en la fase de creación de trabajos en cola o de representación en función del valor *de jobOperation*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S OK; de \_ lo contrario, **HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

> [!Note]  
> **ReportJobProcessingProgress** solo mostrará el progreso del trabajo de impresión XPS si el trabajo de impresión está en la fase de representación o de cola. **ReportJobProcessingProgress** producirá un error si se llama cuando el trabajo de impresión XPS no está en la fase de cola o representación.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EPrintXPSJobOperation**](eprintxpsjoboperation.md)
</dt> <dt>

[**EPrintXPSJobProgress**](eprintxpsjobprogress.md)
</dt> </dl>

 

