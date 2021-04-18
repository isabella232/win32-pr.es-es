---
description: La función OpenPrinter recupera un identificador de la impresora o del servidor de impresión especificado u otros tipos de controladores en el subsistema de impresión.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: Función OpenPrinter (winspool. h)
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
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648415"
---
# <a name="openprinter-function"></a>OpenPrinter función)

La función **OpenPrinter** recupera un identificador de la impresora o del servidor de impresión especificado u otros tipos de controladores en el subsistema de impresión.

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

*pPrinterName* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre de la impresora o el servidor de impresión, el objeto Printer, el XcvMonitor o XcvPort.

Para un objeto de impresora, use: Nombreimpresora, trabajo xxxx. Para un XcvMonitor, use: ServerName, XcvMonitor Nombremonitor. Para un XcvPort, use: ServerName, XcvPort PortName.

Si **es null**, indica el servidor de impresión local.

</dd> <dt>

*phPrinter* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un identificador (no seguro para subprocesos) para el objeto de impresora o servidor de impresión abierto.

El parámetro *phPrinter* puede devolver un identificador de Xcv para su uso con la función XcvData. Para obtener más información sobre XcvData, consulte el DDK.

</dd> <dt>

*pDefault* \[ de\]
</dt> <dd>

Un puntero a una estructura de [**\_ valores predeterminados de impresora**](printer-defaults.md) . Este valor puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Un identificador obtenido para una impresora remota mediante una llamada a **OpenPrinter** para una impresora remota obtiene acceso a la impresora a través de una memoria caché local en el servicio Administrador de trabajos de impresión. Esta caché no es precisa en tiempo real. Para obtener datos precisos, reemplace la llamada a OpenPrinter por [**OpenPrinter2**](openprinter2.md) con POptions. dwFlags establecida en la opción de impresora \_ \_ sin \_ caché. Tenga en cuenta que solo OpenPrinter2W es funcional. La función devuelve un identificador de impresora que utiliza otras llamadas a la API de impresión y omite la memoria caché local. Este método se bloquea mientras se espera la comunicación de red con la impresora remota, por lo que podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. La llamada a esta función desde un subproceso que administra la interacción con la interfaz de usuario puede hacer que la aplicación parezca que no responde.

 

> [!Note]  
> Un identificador obtenido mediante una llamada a **OpenPrinter** para una impresora remota tendrá acceso a la impresora a través de una memoria caché local en el servicio Administrador de trabajos de impresión. Esta caché es, por diseño, no precisa en tiempo real. Si necesita obtener datos precisos, reemplace la llamada a **OpenPrinter** por [**OpenPrinter2**](openprinter2.md) con *pOptions. dwFlags* establecida en la [**opción de impresora \_ \_ sin \_ caché**](printer-options.md). Tenga en cuenta que solo **OpenPrinter2W** es funcional. De este modo, la función devuelve un identificador de impresora que hace que otras llamadas a la API de impresión omitan la memoria caché local. Tenga en cuenta que este enfoque se bloqueará mientras se espera la comunicación de red de ida y vuelta a la impresora remota, por lo que es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Por lo tanto, llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El identificador al que apunta *phPrinter* no es seguro para subprocesos. Si los autores de las llamadas necesitan usarlo simultáneamente en varios subprocesos, deben proporcionar acceso de sincronización personalizado al identificador de la impresora mediante las [funciones de sincronización](/windows/desktop/Sync/synchronization-functions). Para evitar escribir código personalizado, la aplicación puede abrir un identificador de impresora en cada subproceso, según sea necesario.

El parámetro *pDefault* le permite especificar el tipo de datos y los valores de modo de dispositivo que se usan para imprimir documentos enviados por la función [**StartDocPrinter**](startdocprinter.md) . Sin embargo, puede invalidar estos valores mediante la función [**SetJob**](setjob.md) después de haber iniciado un documento.

La configuración de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definida en la estructura de [**\_ valores predeterminados**](printer-defaults.md) de la impresora del parámetro *pDefault* no se usa cuando el valor del miembro *pDatatype* de la estructura [**doc \_ info \_ 1**](doc-info-1.md) que se pasó en el parámetro *pDocInfo* de la llamada [**StartDocPrinter**](startdocprinter.md) es "RAW". Cuando un documento de alto nivel (como un archivo de Adobe PDF o Microsoft Word) u otros datos de impresora (como PCL, PS o HPGL) se envían directamente a una impresora con *pDatatype* establecido en "RAW", el documento debe describir por completo la configuración del trabajo de impresión de estilo **DEVMODE** en el idioma que comprenda el hardware.

Puede llamar a la función **OpenPrinter** para abrir un identificador a un servidor de impresión o para determinar los derechos de acceso que un cliente tiene a un servidor de impresión. Para ello, especifique el nombre del servidor de impresión en el parámetro *pPrinterName* , establezca los miembros **pDatatype** y **pDevMode** de la estructura [**de \_ valores predeterminados**](printer-defaults.md) de la impresora en **null** y establezca el miembro **DesiredAccess** para especificar un valor de máscara de acceso de servidor, como servidor \_ todos los \_ accesos. Cuando termine con el identificador, páselo a la función [**ClosePrinter**](closeprinter.md) para cerrarlo.

Use el miembro **DesiredAccess** de la estructura de [**\_ valores predeterminados**](printer-defaults.md) de la impresora para especificar los derechos de acceso que necesita a la impresora. Los derechos de acceso pueden ser uno de los siguientes. (Si *pDefault* es **null**, los derechos de acceso son Printer \_ uso de acceso \_ ).



| Valor de acceso deseado                        | Significado                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_administrar el acceso a las impresoras \_                 | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md).                                                                                                 |
| \_uso de acceso a impresoras \_                        | Para realizar operaciones de impresión básicas.                                                                                                                                                        |
| \_todo el \_ acceso a la impresora                        | Para realizar todas las tareas administrativas y las operaciones de impresión básicas excepto la sincronización (consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights)).                                     |
| \_acceso limitado de administración de acceso a impresoras \_ \_            | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md) y [**SetPrinterData**](setprinterdata.md). Este valor está disponible a partir de Windows 8.1. |
| valores de seguridad genéricos, como WRITE \_ DAC | Para permitir derechos de acceso de control específicos. Consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Si un usuario no tiene permiso para abrir una impresora o un servidor de impresión especificados con el acceso deseado, se producirá un error en la llamada **OpenPrinter** con un valor devuelto de cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el valor error de \_ acceso \_ denegado.

## <a name="examples"></a>Ejemplos

Para obtener un programa de ejemplo que usa esta función, consulte [Cómo: imprimir con la API de impresión de GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **OpenPrinterW** (Unicode) y **OpenPrinterA** (ANSI)<br/>                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**\_valores predeterminados de impresora**](printer-defaults.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

