---
description: La función EnumJobs recupera información sobre un conjunto especificado de trabajos de impresión para una impresora especificada.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Función EnumJobs (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 57c8416b1c1f5820f632271b0ef0973c76a14be9ef08f24b217ebee441fb29d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056515"
---
# <a name="enumjobs-function"></a>Función EnumJobs

La **función EnumJobs** recupera información sobre un conjunto especificado de trabajos de impresión para una impresora especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador del objeto de impresora cuyos trabajos de impresión enumera la función. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*FirstJob* \[ En\]
</dt> <dd>

Posición de base cero dentro de la cola de impresión del primer trabajo de impresión que se enumerará. Por ejemplo, un valor de 0 especifica que la enumeración debe comenzar en el primer trabajo de impresión de la cola de impresión; Un valor de 9 especifica que la enumeración debe comenzar en el décimo trabajo de impresión de la cola de impresión.

</dd> <dt>

*NoJobs* \[ En\]
</dt> <dd>

Número total de trabajos de impresión que se enumeran.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Tipo de información devuelta en el *búfer pJob.*



| Valor                                                                                                | Significado                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | *pJob* recibe una matriz de [**estructuras JOB INFO \_ \_ 1**](job-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | *pJob* recibe una matriz de [**estructuras JOB INFO \_ \_ 2**](job-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | *pJob* recibe una matriz de [**estructuras JOB INFO \_ \_ 3**](job-info-3.md)<br/> |



 

</dd> <dt>

*pJob* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de estructuras [**JOB \_ INFO \_ 1,**](job-info-1.md) [**JOB INFO \_ \_ 2**](job-info-2.md)o [**JOB INFO \_ \_ 3.**](job-info-3.md) El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y las cadenas u otros datos a los que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame **a EnumJobs** con *cbBuf* establecido en cero. Se produce un error en **EnumJobs,** [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR INSUFFICIENT BUFFER y el parámetro \_ \_ *byteNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer *pJob.*

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados si la función se realiza correctamente. Si se produce un error en la función, la variable recibe el número de bytes necesarios.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras [**JOB \_ INFO \_ 1,**](job-info-1.md) [**JOB INFO \_ \_ 2**](job-info-2.md)o [**JOB INFO \_ \_ 3**](job-info-3.md) devueltas en el *búfer pJob.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

La [**estructura JOB INFO \_ \_ 1**](job-info-1.md) contiene información general del trabajo de impresión; la estructura [**JOB INFO \_ \_ 2**](job-info-2.md) tiene información mucho más detallada. La [**estructura JOB INFO \_ \_ 3**](job-info-3.md) contiene información sobre cómo se vinculan los trabajos.

Para determinar el número de trabajos de impresión en la cola de impresoras, llame a la [**función GetPrinter**](getprinter.md) con el *parámetro Level* establecido en 2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumJobsW** (Unicode) y **EnumJobsA** (ANSI)<br/>                                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ TRABAJO 1**](job-info-1.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ TRABAJO 2**](job-info-2.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ TRABAJO 3**](job-info-3.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

