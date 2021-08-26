---
description: La función GetPrinterData recupera los datos de configuración de la impresora o el servidor de impresión especificados.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Función GetPrinterData (Winspool.h)
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
ms.openlocfilehash: d4cf7d1d1b668974f792c6535f1667f127c78541f4786b32201209553e452c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948795"
---
# <a name="getprinterdata-function"></a>Función GetPrinterData

La **función GetPrinterData** recupera los datos de configuración de la impresora o el servidor de impresión especificados.

En Windows 2000 y versiones posteriores de Windows, llamar a **GetPrinterData** equivale a llamar a [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) con el parámetro *pKeyName* establecido en "PrinterDriverData".

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

*hPrinter* \[ En\]
</dt> <dd>

Identificador del servidor de impresión o impresora para el que la función recupera los datos de configuración. Use la [**función OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pValueName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica los datos que se recuperarán.

En el caso de las impresoras, esta cadena es el nombre de un valor del Registro bajo la clave "PrinterDriverData" de la impresora en el Registro.

En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas enumeradas en la sección Comentarios siguiente.

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un valor que indica el tipo de datos recuperados en *pData*. La función devuelve el tipo especificado en la [**llamada SetPrinterData**](setprinterdata.md) o [**SetPrinterDataEx**](setprinterdataex.md) que almacena los datos. Establezca este parámetro en **NULL** si no necesita el tipo de datos .

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe los datos de configuración.

</dd> <dt>

*nSize* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que *apunta pData.*

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño, en bytes, de los datos de configuración. Si el tamaño de búfer especificado por *nSize* es demasiado pequeño, la función devuelve **ERROR MORE \_ \_ DATA** y *pwNeeded* indica el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **ERROR \_ SUCCESS**. Si se produce un error en la función, el valor devuelto es un valor de error.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

**GetPrinterData recupera** los datos de configuración de impresora establecidos por la [**función SetPrinterDataEx**](setprinterdataex.md) o [**SetPrinterData.**](setprinterdata.md)

**GetPrinterData podría** desencadenar una Windows llamada a [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), que podría escribir en el Registro. Si es así, pueden producirse efectos secundarios, como desencadenar una actualización o actualizar el identificador de evento de impresora 20 en el cliente, si la impresora se comparte en una red.

Si *hPrinter* es un identificador de un servidor de impresión, *pValueName* puede especificar uno de los siguientes valores predefinidos.



| Value                                                               | Comentarios                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ ALLOW \_ USER \_ MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) y versiones posteriores<br/> Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores<br/>                                                                                                    |
| **ARQUITECTURA DE \_ SPLREG**                                            |                                                                                                                                                                                                                                 |
| **SPLREG \_ BEEP \_ ENABLED**                                           |                                                                                                                                                                                                                                 |
| **DIRECTORIO SPLREG \_ PREDETERMINADO \_ SPOOL \_**                               |                                                                                                                                                                                                                                 |
| **NOMBRE DE LA MÁQUINA \_ DNS SPLREG \_ \_**                                      |                                                                                                                                                                                                                                 |
| **SPLREG \_ DS \_ PRESENT**                                             | Si la devolución es correcta, *pData* 0x0001 si la máquina está en un dominio DS; en caso contrario, 0.<br/>                                                                                                                         |
| **SPLREG \_ DS \_ PRESENTES \_ PARA EL \_ USUARIO**                                  | Si la devolución es correcta, *pData* 0x0001 si el usuario ha iniciado sesión en un dominio DS; en caso contrario, 0.<br/>                                                                                                                   |
| **REGISTRO DE EVENTOS \_ SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **VERSIÓN PRINCIPAL DE SPLREG \_ \_**                                          |                                                                                                                                                                                                                                 |
| **VERSIÓN SECUNDARIA DE SPLREG \_ \_**                                          |                                                                                                                                                                                                                                 |
| **VENTANA EMERGENTE DE SPLREG \_ NET \_**                                              | No se admite en Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                       |
| **VENTANA EMERGENTE DE SPLREG \_ NET \_ AL \_ \_ EQUIPO**                                | Si la devolución es correcta, *pData* contiene 1 si se deben enviar notificaciones de trabajo al equipo cliente, o 0 si las notificaciones de trabajo se van a enviar al usuario.<br/> No se admite en Windows Server 2003 y versiones posteriores<br/> |
| **VERSIÓN DEL \_ SISTEMA OPERATIVO SPLREG \_**                                             | Windows XP y versiones posteriores<br/>                                                                                                                                                                                                 |
| **SPLREG \_ OS \_ VERSIONEX**                                           |                                                                                                                                                                                                                                 |
| **VALOR PREDETERMINADO DE \_ PRIORIDAD DEL SUBPROCESO DE PUERTO \_ \_ SPLREG \_**                         |                                                                                                                                                                                                                                 |
| **PRIORIDAD DEL SUBPROCESO \_ DE PUERTO SPLREG \_ \_**                                  |                                                                                                                                                                                                                                 |
| **GRUPOS DE AISLAMIENTO \_ DE CONTROLADORES DE \_ IMPRESIÓN \_ \_ DE SPLREG**                        | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **TIEMPO DE AISLAMIENTO DEL CONTROLADOR DE IMPRESIÓN SPLREG \_ \_ ANTES DEL \_ \_ \_ \_ RECICLAJE**         | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG \_ PRINT \_ DRIVER \_ ISOLATION \_ MAX \_ OBJECTS \_ BEFORE \_ RECYCLE** | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **TIEMPO DE ESPERA DE INACTIVIDAD DE AISLAMIENTO DEL CONTROLADOR DE \_ \_ IMPRESIÓN \_ \_ \_ SPLREG**                 | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **DIRECTIVA DE EJECUCIÓN DE \_ AISLAMIENTO DEL CONTROLADOR DE \_ \_ IMPRESIÓN \_ \_ SPLREG**             | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **DIRECTIVA DE INVALIDACIÓN \_ DE AISLAMIENTO DE CONTROLADOR DE IMPRESIÓN \_ \_ \_ SPLREG \_**              | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **FAX REMOTO de SPLREG \_ \_**                                             | Si la devolución es correcta, *pData* 0x0001 si el servicio FAX admite clientes remotos; en caso contrario, 0.<br/>                                                                                                               |
| **VENTANA EMERGENTE DE REINTENTO DE SPLREG \_ \_**                                            | Si la devolución es correcta, *pData* contiene 1 si el servidor está establecido para volver a intentar ventanas emergentes para todos los trabajos, o 0 si el servidor no vuelve a intentar ventanas emergentes para todos los trabajos.<br/> No se admite en Windows Server 2003 y versiones posteriores<br/> |
| **PRIORIDAD DEL SUBPROCESO \_ DEL PROGRAMADOR \_ DE SPLREG \_**                             |                                                                                                                                                                                                                                 |
| **VALOR PREDETERMINADO DE \_ PRIORIDAD DEL SUBPROCESO DEL PROGRAMADOR \_ \_ DE \_ SPLREG**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                                        |



 

Los siguientes valores de *pValueName indican* el comportamiento de impresión del grupo cuando se produce un error.



| Value                                       | Comentarios                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ RESTART \_ JOB \_ ON \_ POOL \_ ERROR**   | El valor *de pData* indica el tiempo, en segundos, cuando se reinicia un trabajo en otro puerto después de que se produzca un error. Esta configuración se usa con **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ENABLED**.<br/> |
| **TRABAJO DE REINICIO DE SPLREG \_ \_ EN EL GRUPO \_ \_ \_ HABILITADO** | Un valor distinto de cero en *pData* indica que **está habilitado SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR.**<br/>                                                                                            |



 

El tiempo especificado en **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR** es un tiempo mínimo. El tiempo real puede ser mayor, dependiendo de la siguiente configuración del monitor de puerto, que son los valores del Registro en esta clave del Registro:

**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ Ports**

Llame a [**la función RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para consultar estos valores.



| Configuración del monitor de puerto     | Tipo de datos      | Significado                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Si es un valor distinto de cero, permite que el monitor de puerto actualice el colador con el estado del puerto.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Especifica el intervalo, en minutos, cuando el monitor de puerto actualiza el colador con el estado del puerto.<br/> |



 

En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada. Los valores siguientes configuran la representación del lado cliente de un trabajo de impresión y se pueden leer si establece los valores siguientes en *pValueName*.



| Configuración                      | Tipo de datos      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Un valor de 0, o si este valor no está presente en el Registro, habilita la representación predeterminada del lado cliente de los trabajos de impresión.<br/> Un valor de 1 deshabilita la representación del lado cliente de los trabajos de impresión.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG \_ DWORD** | Un valor de 0, o si este valor no está presente en el Registro, hará que los trabajos de impresión se represente en el cliente. Si un trabajo de impresión no se puede representar en el cliente, se representará en el servidor. Si un trabajo de impresión no se puede representar en el servidor, se producirá un error.<br/> Un valor de 1 representará los trabajos de impresión en el cliente. Si un trabajo de impresión no se puede representar en el cliente, se producirá un error.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
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

[**PRINTPROCESSOR \_ CAPS \_ 1**](printprocessor-caps-1.md)
</dt> </dl>

 

