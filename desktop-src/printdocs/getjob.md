---
description: La función GetJob recupera información acerca de un trabajo de impresión especificado.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: Función GetJob (winspool. h)
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
ms.openlocfilehash: 73ae36ebab4530bf21eb86918fdbbbe941ed0741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276779"
---
# <a name="getjob-function"></a>GetJob función)

La función **GetJob** recupera información acerca de un trabajo de impresión especificado.

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora para la que se recuperan los datos del trabajo de impresión. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*JobID* \[ de\]
</dt> <dd>

Identifica el trabajo de impresión para el que se van a recuperar datos. Use la función [**AddJob**](addjob.md) o la función [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obtener un identificador de trabajo de impresión.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Tipo de información que se devuelve en el búfer de *pJob* . Si el *nivel* es 1, *pJob* recibe una estructura [**Job \_ info \_ 1**](job-info-1.md) . Si el *nivel* es 2, *pJob* recibe una estructura [**Job \_ info \_ 2**](job-info-2.md) .

</dd> <dt>

*pJob* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe la información de [**trabajo \_ \_ 1**](job-info-1.md) o una estructura de la [**información de trabajo \_ \_ 2**](job-info-2.md) que contiene información sobre el trabajo. El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame a **GetJob** con *cbBuf* establecido en cero. **GetJob** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, de la matriz.

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Un puntero a un valor que especifica el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

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
| Nombres Unicode y ANSI<br/>   | **GetJobW** (Unicode) y **GetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**Información de trabajo \_ \_ 1**](job-info-1.md)
</dt> <dt>

[**Información de trabajo \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

