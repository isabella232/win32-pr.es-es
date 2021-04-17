---
description: La función GetPrinterData recupera los datos de configuración para la impresora o el servidor de impresión especificado.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Función GetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706705"
---
# <a name="getprinterdata-function"></a>GetPrinterData función)

La función **GetPrinterData** recupera los datos de configuración para la impresora o el servidor de impresión especificado.

En Windows 2000 y versiones posteriores de Windows, llamar a **GetPrinterData** es equivalente a llamar a [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) con el parámetro *pKeyName* establecido en "PrinterDriverData".

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora o del servidor de impresión para el que la función recupera datos de configuración. Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pValueName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que identifica los datos que se van a recuperar.

En el caso de las impresoras, esta cadena es el nombre de un valor del registro en la clave "PrinterDriverData" de la impresora del registro.

En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas que aparecen en la sección Comentarios siguiente.

</dd> <dt>

*pType* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un valor que indica el tipo de datos recuperados en *pdata*. La función devuelve el tipo especificado en la llamada a [**SetPrinterData**](setprinterdata.md) o [**SetPrinterDataEx**](setprinterdataex.md) que almacena los datos. Establezca este parámetro en **null** si no necesita el tipo de datos.

</dd> <dt>

*pdata* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe los datos de configuración.

</dd> <dt>

*nSize* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pdata* .

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño, en bytes, de los datos de configuración. Si el tamaño de búfer especificado por *nSize* es demasiado pequeño, la función devuelve un **error \_ más \_ datos** y *pcbNeeded* indica el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es **error \_ Success**. Si se produce un error en la función, el valor devuelto es un valor de error.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

**GetPrinterData** recupera los datos de configuración de la impresora que se establecieron con la función [**SetPrinterDataEx**](setprinterdataex.md) o [**SetPrinterData**](setprinterdata.md) .

**GetPrinterData** puede desencadenar una llamada de Windows a [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), que puede escribir en el registro. Si lo hace, pueden producirse efectos secundarios, como desencadenar una actualización o actualizar el ID. de evento 20 de la impresora en el cliente, si la impresora se comparte en una red.

Si *hPrinter* es un identificador de un servidor de impresión, *pValueName* puede especificar uno de los siguientes valores predefinidos.



| Value                                                               | Comentarios                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ permitir el \_ usuario \_ MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) y versiones posteriores<br/> Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores<br/>                                                                                                    |
| **arquitectura de SPLREG \_**                                            |                                                                                                                                                                                                                                 |
| **SPLREG \_ beep \_ habilitado**                                           |                                                                                                                                                                                                                                 |
| **\_Directorio de \_ cola de impresión predeterminado de SPLREG \_**                               |                                                                                                                                                                                                                                 |
| **nombre de la \_ máquina DNS SPLREG \_ \_**                                      |                                                                                                                                                                                                                                 |
| **SPLREG \_ DS \_ present**                                             | Si la devolución es correcta, *pdata* contiene 0x0001 si el equipo está en un dominio de DS, de lo contrario, es 0.<br/>                                                                                                                         |
| **SPLREG \_ DS \_ present \_ for \_ User**                                  | Si la devolución es correcta, *pdata* contiene 0x0001 si el usuario ha iniciado sesión en un dominio de DS, de lo contrario, es 0.<br/>                                                                                                                   |
| **\_registro de eventos de SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **\_versión principal de SPLREG \_**                                          |                                                                                                                                                                                                                                 |
| **\_versión secundaria de SPLREG \_**                                          |                                                                                                                                                                                                                                 |
| **\_ \_ menú emergente de SPLREG net**                                              | No se admite en Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                       |
| **SPLREG \_ net \_ popup \_ en el \_ equipo**                                | Si la devolución es correcta, *pdata* contiene 1 si se deben enviar notificaciones de trabajo al equipo cliente, o 0 si las notificaciones de trabajo se van a enviar al usuario.<br/> No se admite en Windows Server 2003 y versiones posteriores<br/> |
| **\_versión de SO SPLREG \_**                                             | Windows XP y versiones posteriores<br/>                                                                                                                                                                                                 |
| **SPLREG \_ os \_ VERSIONEX**                                           |                                                                                                                                                                                                                                 |
| **\_ \_ \_ valor predeterminado de prioridad de subproceso de Puerto SPLREG \_**                         |                                                                                                                                                                                                                                 |
| **\_prioridad de \_ subproceso de Puerto SPLREG \_**                                  |                                                                                                                                                                                                                                 |
| **SPLREG \_ \_ grupos de \_ aislamiento de controladores de impresión \_**                        | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG \_ tiempo de aislamiento de controladores de impresión \_ antes de \_ \_ \_ \_ reciclar**         | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG de \_ aislamiento de controlador de impresión máximo de \_ \_ \_ \_ objetos antes del \_ \_ reciclaje** | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **\_tiempo de \_ \_ espera de \_ inactividad de controlador de impresión SPLREG \_**                 | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG \_ \_ Directiva de \_ ejecución de aislamiento de controladores de \_ impresión \_**             | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG \_ \_ Directiva de \_ \_ invalidación de aislamiento de controladores de impresión \_**              | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **\_fax remoto \_ SPLREG**                                             | Si la devolución es correcta, *pdata* contiene 0x0001 si el servicio de fax admite clientes remotos; de lo contrario, es 0.<br/>                                                                                                               |
| **\_elemento emergente de reintento de SPLREG \_**                                            | Si la devolución es correcta, *pdata* contiene 1 si el servidor está configurado para reintentar ventanas emergentes para todos los trabajos, o 0 si el servidor no reintenta las ventanas emergentes de todos los trabajos.<br/> No se admite en Windows Server 2003 y versiones posteriores<br/> |
| **\_prioridad de \_ subproceso de SPLREG Scheduler \_**                             |                                                                                                                                                                                                                                 |
| **\_ \_ \_ prioridad predeterminada del subproceso de SPLREG Scheduler \_**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                                        |



 

Los siguientes valores de *pValueName* indican el comportamiento de impresión del grupo cuando se produce un error.



| Value                                       | Comentarios                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ error al reiniciar el trabajo \_ de SPLREG en el \_ grupo \_**   | El valor de *pdata* indica el tiempo, en segundos, en el que se reinicia un trabajo en otro puerto después de que se produzca un error. Esta configuración se usa con **el \_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_ habilitado**.<br/> |
| **\_ \_ trabajo de reinicio de SPLREG \_ en \_ grupo \_ habilitado** | Un valor distinto de cero en *pdata* indica que está habilitado el **\_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_** .<br/>                                                                                            |



 

La hora especificada en **el \_ trabajo de reinicio de SPLREG \_ en el \_ \_ \_ error de grupo** es un tiempo mínimo. La hora real puede ser mayor, dependiendo de la configuración del monitor de puerto siguiente, que son valores del registro en esta clave del registro:

**HKLM \\ System \\ CurrentControlSet \\ control \\ Print \\ Monitors \\ < *nombremonitor* > \\ puertos**

Llame a la función [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para consultar estos valores.



| Configuración del monitor de Puerto     | Tipo de datos      | Significado                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **\_valor DWORD reg** | Si es un valor distinto de cero, permite que el monitor de Puerto actualice la cola de impresión con el estado del puerto.<br/>            |
| **StatusUpdateInterval** | **\_valor DWORD reg** | Especifica el intervalo, en minutos, en el que el monitor de Puerto actualiza la cola de impresión con el estado del puerto.<br/> |



 

En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada. Los valores siguientes configuran la representación del lado cliente de un trabajo de impresión y se pueden leer si establece los siguientes valores en *pValueName*.



| Configuración                      | Tipo de datos      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **\_valor DWORD reg** | Un valor de 0, o si este valor no está presente en el registro, habilita la representación del lado cliente predeterminada de los trabajos de impresión.<br/> Un valor de 1 deshabilita la representación del lado cliente de los trabajos de impresión.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **\_valor DWORD reg** | Un valor de 0, o si este valor no está presente en el registro, hará que los trabajos de impresión se representen en el cliente. Si no se puede representar un trabajo de impresión en el cliente, se representará en el servidor. Si no se puede representar un trabajo de impresión en el servidor, se producirá un error.<br/> Un valor de 1 representará los trabajos de impresión en el cliente. Si no se puede representar un trabajo de impresión en el cliente, se producirá un error.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetPrinterDataW** (Unicode) y **GetPrinterDataA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> <dt>

[**PRINTPROCESSOR \_ Cap \_ 1**](printprocessor-caps-1.md)
</dt> </dl>

 

