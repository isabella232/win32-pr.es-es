---
description: La función GetPrinterDataEx recupera los datos de configuración de la impresora o el servidor de impresión especificados.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: Función GetPrinterDataEx (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 146c4f650b646e5b2be9e0ec809221beebe9f596fcb591fe148be615417faa04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034183"
---
# <a name="getprinterdataex-function"></a>Función GetPrinterDataEx

La **función GetPrinterDataEx** recupera los datos de configuración de la impresora o el servidor de impresión especificados. **GetPrinterDataEx puede** recuperar los valores almacenados por la [**función SetPrinterData.**](setprinterdata.md) Además, **GetPrinterDataEx puede** recuperar valores que la función [**SetPrinterDataEx**](setprinterdataex.md) almacena en una clave especificada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
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

*pKeyName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la clave que contiene el valor que se va a recuperar. Use el carácter de barra diagonal inversa ( ) como delimitador para especificar una ruta de \\ acceso que tenga una o varias subclaves.

Si *hPrinter* es un identificador de una impresora y *pKeyName* es **NULL** o una cadena vacía, **GetPrinterDataEx** devuelve **ERROR INVALID \_ \_ PARAMETER**.

Si *hPrinter es* un identificador de un servidor de impresión, se omite *pKeyName.*

</dd> <dt>

*pValueName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica los datos que se recuperarán.

En el caso de las impresoras, esta cadena especifica el nombre de un valor en la *clave pKeyName.*

En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas enumeradas en la sección Comentarios siguiente.

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tipo de datos almacenados en el valor. La función devuelve el tipo especificado en la [**llamada a SetPrinterDataEx**](setprinterdataex.md) cuando se almacenaron los datos. Este parámetro puede ser **NULL** si no necesita la información. **GetPrinterDataEx** pasa *pType* en como el parámetro *lpdwType* de una llamada de [**función RegQueryValueEx.**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa)

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe los datos de configuración.

</dd> <dt>

*nSize* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pData*.

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño, en bytes, de los datos de configuración. Si el tamaño de búfer especificado por *nSize* es demasiado pequeño, la función devuelve **ERROR MORE \_ \_ DATA** y *pwNeeded* indica el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **ERROR \_ SUCCESS**.

Si se produce un error en la función, el valor devuelto es un valor de error.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

**GetPrinterDataEx** recupera los datos de configuración de impresora establecidos por las funciones [**SetPrinterDataEx**](setprinterdataex.md) y [**SetPrinterData.**](setprinterdata.md)

Llamar **a GetPrinterDataEx** con el parámetro *pKeyName* establecido en "PrinterDriverData" equivale a llamar a la [**función GetPrinterData.**](getprinterdata.md)

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



 

Si *pKeyName* es una de las claves predefinidas del servicio de directorio (DS) (vea [**SetPrinter**](setprinter.md)) y *pValueName* contiene una coma (','), la parte de *pValueName* antes de la coma es el nombre del valor y la parte de *pValueName* a la derecha de la coma es el OID de la propiedad DS. Se crea una subclave denominada OID y se introduce un nuevo valor que consta del nombre del valor y el OID en la clave OID. [**SetPrinterDataEx**](setprinterdataex.md) también agrega el nombre del valor y los datos bajo la clave DS.

En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada. La configuración de la representación del lado cliente para una impresora se puede leer estableciendo *pKeyName* en "PrinterDriverData" y *pValueName* en el valor de configuración de la tabla siguiente.



| Configuración                      | Tipo de datos      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Un valor de 0, o si este valor no está presente en el Registro, habilita la representación predeterminada del lado cliente de los trabajos de impresión.<br/> El valor 1 deshabilita la representación del lado cliente de los trabajos de impresión.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG \_ DWORD** | Un valor de 0, o si este valor no está presente en el Registro, hará que los trabajos de impresión se represente en el cliente. Si un trabajo de impresión no se puede representar en el cliente, se representará en el servidor. Si un trabajo de impresión no se puede representar en el servidor, se producirá un error.<br/> Un valor de 1 representará los trabajos de impresión en el cliente. Si un trabajo de impresión no se puede representar en el cliente, se producirá un error.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetPrinterDataExW** (Unicode) y **GetPrinterDataExA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

