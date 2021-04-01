---
description: La función AddJob agrega un trabajo de impresión a la lista de trabajos de impresión que puede programar el administrador de trabajos de impresión. La función recupera el nombre del archivo que puede usar para almacenar el trabajo.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: Función AddJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813571"
---
# <a name="addjob-function"></a>AddJob función)

La función **AddJob** agrega un trabajo de impresión a la lista de trabajos de impresión que puede programar el administrador de trabajos de impresión. La función recupera el nombre del archivo que puede usar para almacenar el trabajo.

> [!NOTE]
> En los sistemas operativos Windows 8 y versiones posteriores, no se recomienda usar **AddJob** directamente porque hay casos (como imprimir en una cola mediante File: o PORTPROMPT:) donde **AddJob** producirá un error. En su lugar, se recomienda usar la [API de impresión de GDI](gdi-printing.md), la [API de impresión XPS](xps-printing.md), [**StartDocPrinter**](startdocprinter.md)o el método adecuado del espacio de nombres [**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing) , dependiendo del escenario de impresión.
>
> Si intenta imprimir en una cola mediante **File:** o **PORTPROMPT:**, **AddJob** devolverá el error no \_ admitido.

## <a name="syntax"></a>Sintaxis

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador que especifica la impresora para el trabajo de impresión. Debe ser una impresora local configurada como una impresora en cola. Si *hPrinter* es un identificador de una conexión de impresora remota, o si la impresora está configurada para impresión directa, se produce un error en la función **AddJob** . Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

La versión de la estructura de datos de la información del trabajo de impresión que la función almacena en el búfer al que apunta *pdata*. Establezca este parámetro en uno.

</dd> <dt>

*pdata* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe una estructura de datos de [**ADDJOB \_ info \_ 1**](addjob-info-1.md) y una cadena de ruta de acceso.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pdata*. El búfer debe ser lo suficientemente grande como para contener una estructura de [**ADDJOB \_ info \_ 1**](addjob-info-1.md) y una cadena de ruta de acceso.

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño total, en bytes, de la estructura de datos [**ADDJOB \_ info \_ 1**](addjob-info-1.md) más la cadena de ruta de acceso. Si este valor es menor o igual que *cbBuf* y la función se ejecuta correctamente, se trata del número real de bytes escritos en el búfer señalado por *pdata*. Si este número es mayor que *cbBuf*, el búfer es demasiado pequeño y debe volver a llamar a la función con un tamaño de búfer de al menos tan grande como \* *pcbNeeded*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Puede llamar a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir el archivo de cola de impresión especificado por el miembro de la **ruta de acceso** de la estructura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) y, a continuación, llamar a la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para escribir en él los datos del trabajo de impresión. Una vez hecho esto, llame a la función [**ScheduleJob**](schedulejob.md) para notificar al administrador de trabajos de impresión que el trabajo de impresión puede ser programado ahora por el administrador de trabajos de impresión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddJobW** (Unicode) y **AddJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ADDJOB \_ info \_ 1**](addjob-info-1.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[API de impresión GDI](gdi-printing.md)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[API de impresión XPS](xps-printing.md)
</dt> </dl>

 

