---
description: La función OpenPrinter recupera un identificador para la impresora o el servidor de impresión especificados u otros tipos de identificadores del subsistema de impresión.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: Función OpenPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 48f25f9c8aec314b997a4600335e22bea2f0bbd8eefa78235ddbb25192f556f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868608"
---
# <a name="openprinter-function"></a>Función OpenPrinter

La **función OpenPrinter** recupera un identificador para la impresora o el servidor de impresión especificados u otros tipos de identificadores del subsistema de impresión.

## <a name="syntax"></a>Sintaxis


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPrinterName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de la impresora o del servidor de impresión, el objeto de impresora, XcvMonitor o XcvPort.

Para un objeto de impresora, use: PrinterName, Job xxxx. Para XcvMonitor, use: ServerName, XcvMonitor MonitorName. Para un XcvPort, use: ServerName, XcvPort PortName.

Si **es NULL,** indica el servidor de impresora local.

</dd> <dt>

*phPrinter* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un identificador (no seguro para subprocesos) al objeto de impresora o servidor de impresión abierto.

El *parámetro phPrinter* puede devolver un identificador Xcv para su uso con la función XcvData. Para obtener más información sobre XcvData, consulte el DDK.

</dd> <dt>

*pDefault* \[ En\]
</dt> <dd>

Puntero a una [**estructura PRINTER \_ DEFAULTS.**](printer-defaults.md) Este valor puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Un identificador obtenido para una impresora remota mediante una llamada a **OpenPrinter** para una impresora remota accede a la impresora a través de una caché local en el servicio de administrador de trabajos de impresión. Esta caché no es precisa en tiempo real. Para obtener datos precisos, reemplace la llamada de [**OpenPrinter por OpenPrinter2**](openprinter2.md) por pOptions.dwFlags establecido en PRINTER \_ OPTION NO \_ \_ CACHE. Tenga en cuenta que solo OpenPrinter2W es funcional. La función devuelve un identificador de impresora que usa otras llamadas a la API de impresión y omite la memoria caché local. Este método se bloquea mientras se espera la comunicación de red con la impresora remota, por lo que es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción de la interfaz de usuario puede hacer que la aplicación parezca no responder.

 

> [!Note]  
> Un identificador obtenido por una llamada a **OpenPrinter** para una impresora remota accederá a la impresora a través de una caché local en el servicio de administrador de trabajos de impresión. Por diseño, esta caché no es precisa en tiempo real. Si necesita obtener datos precisos, reemplace la llamada de **OpenPrinter** por [**OpenPrinter2**](openprinter2.md) por *pOptions.dwFlags* establecido en [**PRINTER OPTION NO \_ \_ \_ CACHE**](printer-options.md). Tenga en cuenta que **solo OpenPrinter2W** es funcional. De este modo, la función devuelve un identificador de impresora que realiza otras llamadas a la API de impresión para omitir la memoria caché local. Tenga en cuenta que este enfoque se bloqueará mientras se espera la comunicación de red de ida y vuelta con la impresora remota, por lo que es posible que no vuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y la implementación del controlador de impresora, factores que son difíciles de predecir al escribir una aplicación. Por lo tanto, llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

El identificador al que apunta *phPrinter no* es seguro para subprocesos. Si los autores de la llamada necesitan usarlo simultáneamente en varios subprocesos, deben proporcionar acceso de sincronización personalizado al identificador de impresora mediante las [funciones de sincronización](/windows/desktop/Sync/synchronization-functions). Para evitar escribir código personalizado, la aplicación puede abrir un identificador de impresora en cada subproceso, según sea necesario.

El *parámetro pDefault* permite especificar los valores de tipo de datos y modo de dispositivo que se usan para imprimir documentos enviados por la [**función StartDocPrinter.**](startdocprinter.md) Sin embargo, puede invalidar estos valores mediante la [**función SetJob**](setjob.md) una vez iniciado un documento.

La configuración [**de DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definida en la estructura [**PRINTER \_ DEFAULTS**](printer-defaults.md) del parámetro *pDefault* no se usa cuando el valor del miembro *pDatatype* de la estructura [**DOC INFO \_ \_ 1**](doc-info-1.md) que se pasó en el *parámetro pDocInfo* de la llamada [**a StartDocPrinter**](startdocprinter.md) es "RAW". Cuando se envía un documento de alto nivel (como un archivo de Adobe PDF o Microsoft Word) u otros datos de impresora (por ejemplo, PCL, PS o HPGL) directamente a una impresora con *pDatatype* establecido en "RAW", el documento debe describir completamente la configuración del trabajo de impresión **de estilo DEVMODE** en el lenguaje comprendido por el hardware.

Puede llamar a la **función OpenPrinter** para abrir un identificador en un servidor de impresión o para determinar los derechos de acceso que un cliente tiene a un servidor de impresión. Para ello, especifique el nombre del servidor de impresión en el parámetro *pPrinterName,* establezca los miembros **pDatatype** y **pDevMode** de la estructura [**PRINTER \_ DEFAULTS**](printer-defaults.md) en **NULL** y establezca el miembro **DesiredAccess** para especificar un valor de máscara de acceso de servidor como SERVER \_ ALL \_ ACCESS. Cuando termine con el identificador, pásallo a la [**función ClosePrinter**](closeprinter.md) para cerrarlo.

Use el **miembro DesiredAccess** de la [**estructura PRINTER \_ DEFAULTS**](printer-defaults.md) para especificar los derechos de acceso que necesita para la impresora. Los derechos de acceso pueden ser uno de los siguientes. (Si *pDefault* es **NULL,** los derechos de acceso son PRINTER \_ USO \_ DE ACCESO).



| Valor de acceso deseado                        | Significado                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADMINISTRACIÓN DE \_ ACCESO DE \_ IMPRESORA                 | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md).                                                                                                 |
| USO DEL \_ ACCESO A \_ LA IMPRESORA                        | Para realizar operaciones de impresión básicas.                                                                                                                                                        |
| ACCESO A \_ TODOS LOS \_ IMPRESORAS                        | Para realizar todas las tareas administrativas y las operaciones de impresión básicas, excepto SYNCHRONIZE (vea [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).                                     |
| ADMINISTRACIÓN LIMITADA \_ DEL ACCESO A LA \_ \_ IMPRESORA            | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md) y [**SetPrinterData**](setprinterdata.md). Este valor está disponible a partir de Windows 8.1. |
| valores de seguridad genéricos, como WRITE \_ DAC | Para permitir derechos de acceso de control específicos. Consulte [Derechos de acceso estándar.](/windows/desktop/SecAuthZ/standard-access-rights)                                                                                      |



 

Si un usuario no tiene permiso para abrir una impresora o un servidor de impresión especificados con el acceso deseado, se producirá un error en la llamada a **OpenPrinter** con un valor devuelto de cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el valor ERROR \_ ACCESS \_ DENIED.

## <a name="examples"></a>Ejemplos

Para obtener un programa de ejemplo que use esta función, [vea Cómo: Imprimir mediante la API de impresión de GDI.](how-to--print-using-the-gdi-print-api.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **OpenPrinterW** (Unicode) y **OpenPrinterA** (ANSI)<br/>                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**VALORES \_ PREDETERMINADOS DE IMPRESORA**](printer-defaults.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

