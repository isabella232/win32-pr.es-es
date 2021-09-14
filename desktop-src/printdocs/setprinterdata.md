---
description: La función SetPrinterData establece los datos de configuración de una impresora o un servidor de impresión.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Función SetPrinterData (Winspool.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268356"
---
# <a name="setprinterdata-function"></a>Función SetPrinterData

La **función SetPrinterData** establece los datos de configuración de una impresora o un servidor de impresión.

Para especificar la clave del Registro en la que se almacenarán los datos, llame a la [**función SetPrinterDataEx.**](setprinterdataex.md) Llamar **a SetPrinterData** equivale a llamar a la función **SetPrinterDataEx** con el *parámetro pKeyName* establecido en "PrinterDriverData".

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

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora o del servidor de impresión para el que la función establece los datos de configuración. Use la [**función OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pValueName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica los datos que se establecerán.

Para las impresoras, esta cadena es el nombre de un valor del Registro bajo la clave "PrinterDriverData" de la impresora en el Registro.

En el caso de los servidores de impresión, esta cadena es una de las cadenas predefinidas enumeradas en la sección Comentarios siguiente.

</dd> <dt>

*Tipo* \[ En\]
</dt> <dd>

Código que indica el tipo de datos al que apunta el *parámetro pData.* Para obtener una lista de los códigos de tipo posibles, vea [Tipos de valor del Registro](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Puntero a una matriz de bytes que contiene los datos de configuración de la impresora.

</dd> <dt>

*cbData* \[ En\]
</dt> <dd>

Tamaño, en bytes, de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **ERROR \_ SUCCESS**.

Si se produce un error en la función, el valor devuelto es un valor de error.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Para recuperar los datos de configuración existentes de una impresora, llame a [**la función GetPrinterDataEx**](getprinterdataex.md) o [**GetPrinterData.**](getprinterdata.md)

Si *hPrinter* es un identificador de un servidor de impresión, *pValueName* puede especificar uno de los siguientes valores predefinidos.



| Value                                                               | Comentarios                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ ALLOW \_ USER \_ MANAGEFORMS**                                | Windows XP con Service Pack 2 (SP2) y versiones posteriores<br/> Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores<br/>                                                                                                    |
| **SPLREG \_ BEEP \_ ENABLED**                                           |                                                                                                                                                                                                                                 |
| **DIRECTORIO SPLREG \_ DEFAULT \_ SPOOL \_**                               |                                                                                                                                                                                                                                 |
| **REGISTRO DE EVENTOS \_ SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **VENTANA EMERGENTE DE SPLREG \_ NET \_**                                              | No se admite en Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                       |
| **VALOR PREDETERMINADO DE \_ PRIORIDAD DEL SUBPROCESO DE PUERTO \_ \_ SPLREG \_**                         |                                                                                                                                                                                                                                 |
| **PRIORIDAD DEL SUBPROCESO DE PUERTO SPLREG \_ \_ \_**                                  |                                                                                                                                                                                                                                 |
| **GRUPOS DE AISLAMIENTO \_ DE CONTROLADORES DE IMPRESIÓN \_ \_ DE \_ SPLREG**                        | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **TIEMPO DE AISLAMIENTO DEL CONTROLADOR DE IMPRESIÓN SPLREG \_ \_ ANTES DEL \_ \_ \_ \_ RECICLAJE**         | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **SPLREG \_ PRINT \_ DRIVER \_ ISOLATION \_ MAX \_ OBJECTS \_ BEFORE \_ RECYCLE** | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **TIEMPO DE ESPERA DE \_ INACTIVIDAD DE \_ AISLAMIENTO DEL CONTROLADOR DE IMPRESIÓN \_ \_ \_ SPLREG**                 | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **DIRECTIVA DE EJECUCIÓN DE \_ AISLAMIENTO DEL CONTROLADOR DE IMPRESIÓN \_ \_ \_ SPLREG \_**             | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **DIRECTIVA DE INVALIDACIÓN \_ DEL AISLAMIENTO DEL CONTROLADOR DE IMPRESIÓN \_ \_ \_ SPLREG \_**              | Windows 7 y versiones posteriores<br/>                                                                                                                                                                                                  |
| **VENTANA EMERGENTE DE REINTENTO DE SPLREG \_ \_**                                            | Si la devolución es correcta, *pData* contiene 1 si el servidor está configurado para volver a intentar ventanas emergentes para todos los trabajos, o 0 si el servidor no vuelve a intentar ventanas emergentes para todos los trabajos.<br/> No se admite en Windows Server 2003 y versiones posteriores<br/> |
| **PRIORIDAD DE \_ SUBPROCESOS DEL PROGRAMADOR \_ DE SPLREG \_**                             |                                                                                                                                                                                                                                 |
| **SPLREG \_ SCHEDULER \_ THREAD \_ PRIORITY \_ DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 y versiones posteriores<br/>                                                                                                                                                                                        |



 

Los siguientes valores de *pValueName determinan* el comportamiento de impresión del grupo cuando se produce un error.



| Value                                       | Comentarios                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ERROR DE REINICIO DE SPLREG \_ \_ EN EL \_ \_ \_ GRUPO**   | El valor *de pData* indica el tiempo, en segundos, cuando se reinicia un trabajo en otro puerto después de que se produzca un error. Esta configuración se usa con **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ENABLED**.<br/> |
| **TRABAJO DE REINICIO DE SPLREG \_ \_ EN EL GRUPO \_ \_ \_ HABILITADO** | Un valor distinto de cero en *pData* indica que **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR** está habilitado.<br/>                                                                                            |



 

El tiempo especificado en **SPLREG \_ RESTART JOB ON POOL \_ \_ \_ \_ ERROR** es un tiempo mínimo. El tiempo real puede ser mayor, dependiendo de la siguiente configuración del monitor de puerto, que son los valores del Registro bajo esta clave del Registro:

**HKLM \\ SYSTEM \\ CurrentControlSet \\ Control Print Monitors Monitor \\ \\ \\ < *Ports* > \\**

Llame a [**la función RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) para establecer estos valores.



| Configuración del monitor de puerto     | Tipo de datos      | Significado                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG \_ DWORD** | Si es un valor distinto de cero, permite que el monitor de puerto actualice el colador con el estado del puerto.<br/>            |
| **StatusUpdateInterval** | **REG \_ DWORD** | Especifica el intervalo, en minutos, cuando el monitor de puerto actualiza el colador con el estado del puerto.<br/> |



 

En Windows 7 y versiones posteriores de Windows, los trabajos de impresión que se envían a un servidor de impresión se representan en el cliente de forma predeterminada. La representación del lado cliente de un trabajo de impresión se puede configurar para cada impresora estableciendo los siguientes valores en *pValueName*.



| Configuración                      | Tipo de datos      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG \_ DWORD** | Un valor de 0, o si este valor no está presente en el Registro, habilita la representación predeterminada del lado cliente de los trabajos de impresión.<br/> El valor 1 deshabilita la representación del lado cliente de los trabajos de impresión.<br/>                                                                                                                                                                                                      |
| **ForceClientSideRendering** | **REG \_ DWORD** | Un valor de 0, o si este valor no está presente en el Registro, hace que los trabajos de impresión se represente en el cliente. Si un trabajo de impresión no se puede representar en el cliente, se representará en el servidor. Si un trabajo de impresión no se puede representar en el servidor, se producirá un error.<br/> Un valor de 1 representará los trabajos de impresión en el cliente. Si un trabajo de impresión no se puede representar en el cliente, se producirá un error.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **SetPrinterDataW** (Unicode) y **SetPrinterDataA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Consulte también

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

 

