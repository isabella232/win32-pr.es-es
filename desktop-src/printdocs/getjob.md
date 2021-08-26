---
description: La función GetJob recupera información sobre un trabajo de impresión especificado.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: Función GetJob (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 26665d6141ea36adbe8aeeca0555bc6a5e918cb5213a4fb7a6dbd315eac92a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949094"
---
# <a name="getjob-function"></a>Función GetJob

La **función GetJob** recupera información sobre un trabajo de impresión especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora para la que se recuperan los datos del trabajo de impresión. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*JobId* \[ En\]
</dt> <dd>

Identifica el trabajo de impresión para el que se recuperan los datos. Use la [**función AddJob**](addjob.md) o [**startDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obtener un identificador de trabajo de impresión.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Tipo de información devuelta en el *búfer pJob.* Si *Level* es 1, *pJob* recibe una [**estructura JOB INFO \_ \_ 1.**](job-info-1.md) Si *Level* es 2, *pJob* recibe una [**estructura JOB INFO \_ \_ 2.**](job-info-2.md)

</dd> <dt>

*pJob* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una estructura [**JOB \_ INFO \_ 1**](job-info-1.md) o [**JOB INFO \_ \_ 2**](job-info-2.md) que contiene información sobre el trabajo. El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame **a GetJob** con *cbBuf* establecido en cero. **GetJob** produce un error, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR INSUFFICIENT BUFFER y el parámetro \_ \_ *byteNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, de la matriz.

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a un valor que especifica el número de bytes copiados si la función se realiza correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

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
| Nombres Unicode y ANSI<br/>   | **GetJobW** (Unicode) y **GetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ TRABAJO 1**](job-info-1.md)
</dt> <dt>

[**INFORMACIÓN \_ DE \_ TRABAJO 2**](job-info-2.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

