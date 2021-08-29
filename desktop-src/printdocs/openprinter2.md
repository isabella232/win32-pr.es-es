---
description: Recupera un identificador para la impresora, el servidor de impresión u otros tipos de identificadores especificados en el subsistema de impresión, al tiempo que establece algunas de las opciones de impresora.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: Función OpenPrinter2 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 132e7225850899cb33ff815c2fce309fd70a9d288839da2bbf20a6e9f8aafc50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776505"
---
# <a name="openprinter2-function"></a>Función OpenPrinter2

Recupera un identificador para la impresora, el servidor de impresión u otros tipos de identificadores especificados en el subsistema de impresión, al tiempo que establece algunas de las opciones de impresora.

## <a name="syntax"></a>Sintaxis


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPrinterName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en null constante que especifica el nombre de la impresora o del servidor de impresión, el objeto de impresora, XcvMonitor o XcvPort.

Para un objeto de impresora, use: PrinterName,Job xxxx. Para XcvMonitor, use: ServerName,XcvMonitor MonitorName. Para un XcvPort, use: ServerName,XcvPort PortName.

**Windows Vista:** Si **es NULL,** indica el servidor de impresión local.

</dd> <dt>

*phPrinter* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un identificador para la impresora abierta o el objeto de servidor de impresión.

</dd> <dt>

*pDefault* \[ En\]
</dt> <dd>

Puntero a una [**estructura PRINTER \_ DEFAULTS.**](printer-defaults.md) Este valor puede ser **NULL.**

</dd> <dt>

*pOptions* \[ En\]
</dt> <dd>

Puntero a una [**estructura PRINTER \_ OPTIONS.**](printer-options.md) Este valor puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

La versión ANSI de esta función no se implementa y devuelve ERROR \_ NOT \_ SUPPORTED.

El *parámetro pDefault* permite especificar los valores de tipo de datos y modo de dispositivo que se usan para imprimir documentos enviados por la [**función StartDocPrinter.**](startdocprinter.md) Sin embargo, puede invalidar estos valores mediante la [**función SetJob**](setjob.md) una vez iniciado un documento.

Puede llamar a la **función OpenPrinter2** para abrir un identificador en un servidor de impresión o para determinar los derechos de acceso del cliente a un servidor de impresión. Para ello, especifique el nombre del servidor de impresión en el parámetro *pPrinterName,* establezca los miembros **pDatatype** y **pDevMode** de la estructura [**PRINTER \_ DEFAULTS**](printer-defaults.md) en **NULL** y establezca el miembro **DesiredAccess** para especificar un valor de máscara de acceso de servidor como SERVER \_ ALL \_ ACCESS. Cuando haya terminado con el identificador, pásallo a la [**función ClosePrinter**](closeprinter.md) para cerrarlo.

Use el **miembro DesiredAccess** de la [**estructura PRINTER \_ DEFAULTS**](printer-defaults.md) para especificar los derechos de acceso necesarios. Los derechos de acceso pueden ser uno de los siguientes.



| Valor de acceso deseado                        | Significado                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADMINISTRACIÓN DE \_ ACCESO DE \_ IMPRESORA                 | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md).                                                                                                 |
| USO DEL \_ ACCESO A \_ LA IMPRESORA                        | Para realizar operaciones de impresión básicas.                                                                                                                                                        |
| ACCESO A \_ TODOS LOS \_ IMPRESORAS                        | Para realizar todas las tareas administrativas y las operaciones de impresión básicas, excepto SYNCHRONIZE. Consulte [Derechos de acceso estándar.](/windows/desktop/SecAuthZ/standard-access-rights)                                         |
| ADMINISTRACIÓN LIMITADA \_ DEL ACCESO A LA \_ \_ IMPRESORA            | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md) y [**SetPrinterData**](setprinterdata.md). Este valor está disponible a partir de Windows 8.1. |
| valores de seguridad genéricos, como WRITE \_ DAC | Para permitir derechos de acceso de control específicos. Consulte [Derechos de acceso estándar.](/windows/desktop/SecAuthZ/standard-access-rights)                                                                                      |



 

Si un usuario no tiene permiso para abrir una impresora o un servidor de impresión especificados con el acceso deseado, se producirá un error en la llamada a **OpenPrinter2** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el valor ERROR \_ ACCESS \_ DENIED.

Cuando *pPrinterName* es una impresora local, **OpenPrinter2** omite todos los valores de **dwFlags** a los que apuntaba la estructura [**PRINTER \_ OPTIONS**](printer-options.md) mediante *pOptions,* excepto PRINTER \_ OPTION CLIENT \_ \_ CHANGE. Si se pasa este último, **OpenPrinter2** devolverá ERROR \_ ACCESS \_ DENIED. En consecuencia, al abrir una impresora local, **OpenPrinter2** no proporciona ninguna ventaja sobre [**OpenPrinter**](openprinter.md).

**Windows Vista:** Los datos de impresora devueltos por **OpenPrinter2** se recuperan de una caché local a menos que la marca **PRINTER OPTION NO \_ \_ \_ CACHE** esté establecida en el **campo dwFlags** de la estructura [**PRINTER \_ OPTIONS**](printer-options.md) a la que hace referencia *pOptions.*

## <a name="examples"></a>Ejemplos

En este ejemplo, Se produce un error en **OpenPrinter2** cuando PRINTER ACCESS MANAGE LIMITED se pasa a la estructura \_ PRINTER \_ \_ [**\_ DEFAULTS**](printer-defaults.md) y el usuario no tiene el permiso adecuado.


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



Para obtener un programa de ejemplo que muestra cómo usar esta función, vea [Cómo: Imprimir mediante la API de impresión de GDI.](how-to--print-using-the-gdi-print-api.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **OpenPrinter2W** (Unicode) y **OpenPrinter2A** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**VALORES \_ PREDETERMINADOS DE IMPRESORA**](printer-defaults.md)
</dt> <dt>

[**OPCIONES DE \_ IMPRESORA**](printer-options.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

