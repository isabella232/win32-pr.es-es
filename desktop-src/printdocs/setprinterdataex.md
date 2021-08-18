---
description: La función SetPrinterDataEx establece los datos de configuración de una impresora o un servidor de impresión. La función almacena los datos de configuración en la clave del Registro de impresoras.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Función SetPrinterDataEx (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 6d2904c853510efeb379c9d590852c8f082a4644315560c4dfa5a7f51daca6ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460355"
---
# <a name="setprinterdataex-function"></a>Función SetPrinterDataEx

La **función SetPrinterDataEx** establece los datos de configuración de una impresora o un servidor de impresión. La función almacena los datos de configuración en la clave del Registro de la impresora.

## <a name="syntax"></a>Sintaxis


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora o del servidor de impresión para el que la función establece los datos de configuración. Use la [**función OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pKeyName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la clave que contiene el valor que se establecerá. Si la clave o subclaves especificadas no existen, la función las crea.

Para almacenar los datos de configuración que se pueden publicar en el servicio de directorio (DS), especifique una de las siguientes claves predefinidas del Registro.



| Value                                                                                                                                                                      | Significado                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <dt>**SPLDS_DRIVER_KEY**</dt> </dl>    | Los controladores de impresora usan esta clave para almacenar las propiedades del controlador.<br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <dt>**SPLDS_SPOOLER_KEY**</dt> </dl> | Reservado. Solo lo usa el colador de impresión para almacenar las propiedades internas del colador.<br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <dt>**SPLDS_USER_KEY**</dt> </dl>          | Las aplicaciones usan esta clave para almacenar propiedades de impresora, como números de recursos de impresora.<br/> |



 

Los valores almacenados en la SPLDS_USER_KEY se publican en el servicio de directorio solo si hay una propiedad correspondiente en el esquema. Un administrador de dominio debe crear la propiedad si aún no existe. Para publicar una propiedad definida por el usuario después de usar **SetPrinterDataEx** para agregar o cambiar un valor, llame a [**SetPrinter**](setprinter.md) con *Level* = 7 y con el **miembro dwAction** de [**PRINTER_INFO_7**](printer-info-7.md) establecido **en DSPRINT_UPDATE**.

Puede especificar otras claves para almacenar datos de configuración que no son DS. Use el carácter de barra diagonal inversa ( ) como delimitador para especificar una ruta de \\ acceso que tenga una o varias subclaves.

Si *hPrinter es* un identificador de una impresora y *pKeyName* es **NULL** o una cadena vacía, **SetPrinterDataEx** **devuelve ERROR_INVALID_PARAMETER**.

Si *hPrinter es* un identificador de un servidor de impresión, se omite *pKeyName.*

No **use** SPLDS_SPOOLER_KEY . Para cambiar las propiedades de la impresora del colador, use [**SetPrinter**](setprinter.md) con *Nivel* = 2.

</dd> <dt>

*pValueName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica los datos que se establecerán.

En el caso de las impresoras, esta cadena especifica el nombre de un valor en la *clave pKeyName.*

En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas enumeradas en la sección Comentarios siguiente.

</dd> <dt>

*Tipo* \[ En\]
</dt> <dd>

Código que indica el tipo de datos a los que apunta el *parámetro pData.* Para obtener una lista de los códigos de tipo posibles, vea [Tipos de valor del Registro](/windows/desktop/SysInfo/registry-value-types).

Si *pKeyName especifica* una de las claves de servicio de directorio predefinidas, *type* debe ser **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** o **REG_BINARY**. Si **REG_BINARY** se usa , *cbData* debe ser igual a 1 y el servicio de directorio trata los datos como un valor booleano.

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene los datos de configuración de la impresora.

</dd> <dt>

*cbData* \[ En\]
</dt> <dd>

Tamaño, en bytes, de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **ERROR_SUCCESS**.

Si se produce un error en la función, el valor devuelto es un valor de error.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Para recuperar los datos de configuración existentes para una impresora o un administrador de trabajos de impresión, llame a la [**función GetPrinterDataEx.**](getprinterdataex.md)

Llamar **a SetPrinterDataEx** con el parámetro *pKeyName* establecido en "PrinterDriverData" equivale a llamar a la [**función SetPrinterData.**](setprinterdata.md)

Si *hPrinter* es un identificador de un servidor de impresión, *pValueName* puede especificar uno de los siguientes valores predefinidos.



| Value                                                               | Comentarios                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_ALLOW_USER_MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) y versiones posteriores<br/> Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores<br/>                                                                                                    |
| **SPLREG_BEEP_ENABLED**                                           |                                                                                                                                                                                                                                 |
| **SPLREG_DEFAULT_SPOOL_DIRECTORY**                               |                                                                                                                                                                                                                                 |
| **SPLREG_EVENT_LOG**                                              |                                                                                                                                                                                                                                 |
| **SPLREG_NET_POPUP**                                              | No se admite en Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                       |
| **SPLREG_PORT_THREAD_PRIORITY_DEFAULT**                         |                                                                                                                                                                                                                                 |
| **SPLREG_PORT_THREAD_PRIORITY**                                  |                                                                                                                                                                                                                                 |
| **SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**                        | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**         | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE** | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**                 | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**             | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**              | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG_RETRY_POPUP**                                            | Si la devolución es correcta, *pData* contiene 1 si el servidor está establecido para volver a intentar ventanas emergentes para todos los trabajos, o 0 si el servidor no vuelve a intentar ventanas emergentes para todos los trabajos.<br/> No se admite en Windows Server 2003 y versiones posteriores<br/> |
| **SPLREG_SCHEDULER_THREAD_PRIORITY**                             |                                                                                                                                                                                                                                 |
| **SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG_WEBSHAREMGMT**                                            | Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                                        |



 

Si se pasa uno de los siguientes valores predefinidos como *pValueName,* se establece el comportamiento de impresión del grupo cuando se produce un error.



| Value                                       | Comentarios                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_RESTART_JOB_ON_POOL_ERROR**   | El valor *de pData* indica el tiempo, en segundos, cuando se reinicia un trabajo en otro puerto después de que se produzca un error. Esta configuración se usa con **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.<br/> |
| **SPLREG_RESTART_JOB_ON_POOL_ENABLED** | Un valor distinto de cero en *pData* indica que **SPLREG_RESTART_JOB_ON_POOL_ERROR** está habilitado.<br/>                                                                                            |



 

El tiempo especificado en **SPLREG_RESTART_JOB_ON_POOL_ERROR** es un tiempo mínimo. El tiempo real puede ser mayor, dependiendo de la siguiente configuración del monitor de puerto, que son los valores del Registro en esta clave del Registro:

**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Print \\ Monitors \\ < *MonitorName* > \\ Ports**

Llame a [**la función RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) para establecer estos valores.



| Configuración del monitor de puerto     | Tipo de datos      | Significado                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG_DWORD** | Si es un valor distinto de cero, permite que el monitor de puerto actualice el colador con el estado del puerto.<br/>            |
| **StatusUpdateInterval** | **REG_DWORD** | Especifica el intervalo, en minutos, cuando el monitor de puerto actualiza el colador con el estado del puerto.<br/> |



 

Para asegurarse de que el administrador de trabajos redirige los trabajos a la siguiente impresora disponible en el grupo (cuando el trabajo de impresión no se imprime dentro del tiempo establecido), el monitor de puertos debe admitir SNMP y los puertos de red del grupo deben configurarse como "Estado SNMP habilitado". El monitor de puerto que admite SNMP es el monitor de puerto TCP/IP estándar.

En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada. La representación del lado cliente de trabajos de impresión se puede configurar estableciendo *pKeyName* en "PrinterDriverData" y *pValueName* en el valor de configuración de la tabla siguiente.



| Configuración                      | Tipo de datos      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG_DWORD** | Un valor de 0, o si este valor no está presente en el Registro, habilita la representación predeterminada del lado cliente de los trabajos de impresión.<br/> El valor 1 deshabilita la representación del lado cliente de los trabajos de impresión.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG_DWORD** | Un valor de 0, o si este valor no está presente en el Registro, hará que los trabajos de impresión se represente en el cliente. Si un trabajo de impresión no se puede representar en el cliente, se representará en el servidor. Si un trabajo de impresión no se puede representar en el servidor, se producirá un error.<br/> Un valor de 1 representará los trabajos de impresión en el cliente. Si un trabajo de impresión no se puede representar en el cliente, se producirá un error.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **SetPrinterDataExW** (Unicode) y **SetPrinterDataExA** (ANSI)<br/>                               |



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

[**PRINTER_INFO_7**](printer-info-7.md)
</dt> </dl>

 

