---
description: La función EnumJobs recupera información acerca de un conjunto especificado de trabajos de impresión para una impresora especificada.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Función EnumJobs (winspool. h)
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
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277825"
---
# <a name="enumjobs-function"></a>EnumJobs función)

La función **EnumJobs** recupera información acerca de un conjunto especificado de trabajos de impresión para una impresora especificada.

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador del objeto de impresora cuyos trabajos de impresión enumera la función. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*FirstJob* \[ de\]
</dt> <dd>

Posición de base cero dentro de la cola de impresión del primer trabajo de impresión que se va a enumerar. Por ejemplo, un valor de 0 especifica que la enumeración debe comenzar en el primer trabajo de impresión de la cola de impresión; un valor de 9 especifica que la enumeración debe comenzar en el décimo trabajo de impresión en la cola de impresión.

</dd> <dt>

*Nojobs* \[ de\]
</dt> <dd>

Número total de trabajos de impresión que se van a enumerar.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Tipo de información que se devuelve en el búfer de *pJob* .



| Value                                                                                                | Significado                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | *pJob* recibe una matriz de estructuras de [**información de trabajo \_ \_ 1**](job-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | *pJob* recibe una matriz de estructuras [**Job \_ info \_ 2**](job-info-2.md) .<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | *pJob* recibe una matriz de estructuras [**Job \_ info \_ 3**](job-info-3.md) .<br/> |



 

</dd> <dt>

*pJob* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe una matriz de las estructuras Job [**\_ info \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 3**](job-info-3.md) . El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y cualquier cadena u otros datos a los que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame a **EnumJobs** con *cbBuf* establecido en cero. **EnumJobs** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pJob* .

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados si la función se ejecuta correctamente. Si se produce un error en la función, la variable recibe el número de bytes necesarios.

</dd> <dt>

*pcReturned* \[ enuncia\]
</dt> <dd>

Un puntero a una variable que recibe el número de las estructuras Job [**\_ info \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)o [**Job \_ info \_ 3**](job-info-3.md) devueltas en el búfer de *pJob* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

La estructura [**Job \_ info \_ 1**](job-info-1.md) contiene información general sobre el trabajo de impresión; la estructura de la información de [**trabajo \_ \_ 2**](job-info-2.md) tiene información mucho más detallada. La estructura [**Job \_ info \_ 3**](job-info-3.md) contiene información sobre cómo se vinculan los trabajos.

Para determinar el número de trabajos de impresión en la cola de la impresora, llame a la función [**GetPrinter**](getprinter.md) con el parámetro *LEVEL* establecido en 2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

[**Información de trabajo \_ \_ 1**](job-info-1.md)
</dt> <dt>

[**Información de trabajo \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**Información de trabajo \_ \_ 3**](job-info-3.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

