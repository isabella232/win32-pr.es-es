---
description: Notifica al servicio Administrador de trabajos de impresión si un trabajo de impresión XPS está en cola o en la fase de representación y qué parte del procesamiento está en curso actualmente.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Función ReportJobProcessingProgress (winspool. h)
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
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002403"
---
# <a name="reportjobprocessingprogress-function"></a>ReportJobProcessingProgress función)

Notifica al servicio Administrador de trabajos de impresión si un trabajo de impresión XPS está en cola o en la fase de representación y qué parte del procesamiento está en curso actualmente.

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

*printerHandle* \[ de\]
</dt> <dd>

Identificador de impresora para el que la función va a recuperar información. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*jobId* \[in\]
</dt> <dd>

Identifica el trabajo de impresión para el que se van a recuperar datos. Use la función [**AddJob**](addjob.md) o la función [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obtener un identificador de trabajo de impresión.

</dd> <dt>

*jobOperation* 
</dt> <dd>

Especifica si el trabajo está en la fase de puesta en cola o en la fase de representación.

</dd> <dt>

*jobProgress* 
</dt> <dd>

Especifica qué parte del procesamiento está en curso actualmente. Este valor hace referencia a los eventos de la fase de puesta en cola o de representación, en función del valor de *jobOperation*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

> [!Note]  
> **ReportJobProcessingProgress** solo notificará el progreso del trabajo de impresión XPS si el trabajo de impresión se encuentra en la fase de puesta en cola o representación. **ReportJobProcessingProgress** producirá un error si se llama cuando el trabajo de impresión XPS no está en la fase de puesta en cola o representación.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
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

 

