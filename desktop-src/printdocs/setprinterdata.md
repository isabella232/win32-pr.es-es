---
description: La función SetPrinterData establece los datos de configuración de una impresora o un servidor de impresión.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Función SetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909369"
---
# <a name="setprinterdata-function"></a>SetPrinterData función)

La función **SetPrinterData** establece los datos de configuración de una impresora o un servidor de impresión.

Para especificar la clave del registro en la que se almacenan los datos, llame a la función [**SetPrinterDataEx**](setprinterdataex.md) . Llamar a **SetPrinterData** es equivalente a llamar a la función **SetPrinterDataEx** con el parámetro *pKeyName* establecido en "PrinterDriverData".

## <a name="syntax"></a>Sintaxis


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora o del servidor de impresión para el que la función establece los datos de configuración. Use la función [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pValueName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que identifica los datos que se van a establecer.

En el caso de las impresoras, esta cadena es el nombre de un valor del registro en la clave "PrinterDriverData" de la impresora del registro.

En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas que aparecen en la sección Comentarios siguiente.

</dd> <dt>

*Tipo* \[ de de\]
</dt> <dd>

Código que indica el tipo de datos al que apunta el parámetro *pdata* . Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

*pdata* \[ de\]
</dt> <dd>

Puntero a una matriz de bytes que contiene los datos de configuración de la impresora.

</dd> <dt>

*cbData* \[ de\]
</dt> <dd>

Tamaño, en bytes, de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es **error \_ Success**.

Si se produce un error en la función, el valor devuelto es un valor de error.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Para recuperar los datos de configuración existentes de una impresora, llame a la función [**GetPrinterDataEx**](getprinterdataex.md) o [**GetPrinterData**](getprinterdata.md) .

Si *hPrinter* es un identificador de un servidor de impresión, *pValueName* puede especificar uno de los siguientes valores predefinidos.



| Value                                                               | Comentarios                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ permitir el \_ usuario \_ MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) y versiones posteriores<br/> Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores<br/>                                                                                                    |
| **SPLREG \_ beep \_ habilitado**                                           |                                                                                                                                                                                                                                 |
| **\_Directorio de \_ cola de impresión predeterminado de SPLREG \_**                               |                                                                                                                                                                                                                                 |
| **\_registro de eventos de SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **\_ \_ menú emergente de SPLREG net**                                              | No se admite en Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                       |
| **\_ \_ \_ valor predeterminado de prioridad de subproceso de Puerto SPLREG \_**                         |                                                                                                                                                                                                                                 |
| **\_prioridad de \_ subproceso de Puerto SPLREG \_**                                  |                                                                                                                                                                                                                                 |
| **SPLREG \_ \_ grupos de \_ aislamiento de controladores de impresión \_**                        | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG \_ tiempo de aislamiento de controladores de impresión \_ antes de \_ \_ \_ \_ reciclar**         | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG de \_ aislamiento de controlador de impresión máximo de \_ \_ \_ \_ objetos antes del \_ \_ reciclaje** | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **\_tiempo de \_ \_ espera de \_ inactividad de controlador de impresión SPLREG \_**                 | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG \_ \_ Directiva de \_ ejecución de aislamiento de controladores de \_ impresión \_**             | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG \_ \_ Directiva de \_ \_ invalidación de aislamiento de controladores de impresión \_**              | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **\_elemento emergente de reintento de SPLREG \_**                                            | Si la devolución es correcta, *pdata* contiene 1 si el servidor está configurado para reintentar ventanas emergentes para todos los trabajos, o 0 si el servidor no reintenta las ventanas emergentes de todos los trabajos.<br/> No se admite en Windows Server 2003 y versiones posteriores<br/> |
| **\_prioridad de \_ subproceso de SPLREG Scheduler \_**                             |                                                                                                                                                                                                                                 |
| **\_ \_ \_ prioridad predeterminada del subproceso de SPLREG Scheduler \_**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                                        |



 

Los siguientes valores de *pValueName* determinan el comportamiento de impresión del grupo cuando se produce un error.



| Value                                       | Comentarios                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ error al reiniciar el trabajo \_ de SPLREG en el \_ grupo \_**   | El valor de *pdata* indica el tiempo, en segundos, en el que se reinicia un trabajo en otro puerto después de que se produzca un error. Esta configuración se usa con **el \_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_ habilitado**.<br/> |
| **\_ \_ trabajo de reinicio de SPLREG \_ en \_ grupo \_ habilitado** | Un valor distinto de cero en *pdata* indica que está habilitado el **\_ \_ trabajo de reinicio de SPLREG en el \_ \_ grupo \_** .<br/>                                                                                            |



 

La hora especificada en **el \_ trabajo de reinicio de SPLREG \_ en el \_ \_ \_ error de grupo** es un tiempo mínimo. La hora real puede ser mayor, dependiendo de la configuración del monitor de puerto siguiente, que son valores del registro en esta clave del registro:

**HKLM \\ System \\ CurrentControlSet \\ control \\ Print \\ Monitors \\ < *nombremonitor* > \\ puertos**

Llame a la función [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) para establecer estos valores.



| Configuración del monitor de Puerto     | Tipo de datos      | Significado                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **\_valor DWORD reg** | Si es un valor distinto de cero, permite que el monitor de Puerto actualice la cola de impresión con el estado del puerto.<br/>            |
| **StatusUpdateInterval** | **\_valor DWORD reg** | Especifica el intervalo, en minutos, en el que el monitor de Puerto actualiza la cola de impresión con el estado del puerto.<br/> |



 

En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada. La representación del lado cliente de un trabajo de impresión se puede configurar para cada impresora mediante el establecimiento de los siguientes valores en *pValueName*.



| Configuración                      | Tipo de datos      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **\_valor DWORD reg** | Un valor de 0, o si este valor no está presente en el registro, habilita la representación del lado cliente predeterminada de los trabajos de impresión.<br/> Un valor de 1 deshabilita la representación del lado cliente de los trabajos de impresión.<br/>                                                                                                                                                                                                      |
| **ForceClientSideRendering** | **\_valor DWORD reg** | Un valor de 0, o si este valor no está presente en el registro, hace que los trabajos de impresión se representen en el cliente. Si no se puede representar un trabajo de impresión en el cliente, se representará en el servidor. Si no se puede representar un trabajo de impresión en el servidor, se producirá un error.<br/> Un valor de 1 representará los trabajos de impresión en el cliente. Si no se puede representar un trabajo de impresión en el cliente, se producirá un error.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **SetPrinterDataW** (Unicode) y **SetPrinterDataA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

