---
description: Recupera un identificador de la impresora, el servidor de impresión u otros tipos de controladores del subsistema de impresión especificados, mientras se establecen algunas de las opciones de la impresora.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: Función OpenPrinter2 (winspool. h)
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
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910486"
---
# <a name="openprinter2-function"></a>OpenPrinter2 función)

Recupera un identificador de la impresora, el servidor de impresión u otros tipos de controladores del subsistema de impresión especificados, mientras se establecen algunas de las opciones de la impresora.

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

*pPrinterName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de la impresora o el servidor de impresión, el objeto de impresora, el XcvMonitor o XcvPort.

Para un objeto de impresora, use: Nombreimpresora, trabajo xxxx. Para un XcvMonitor, use: ServerName, XcvMonitor Nombremonitor. Para un XcvPort, use: ServerName, XcvPort PortName.

**Windows Vista:** Si **es null**, indica el servidor de impresión local.

</dd> <dt>

*phPrinter* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un identificador para el objeto de impresora o de servidor de impresión abierto.

</dd> <dt>

*pDefault* \[ de\]
</dt> <dd>

Un puntero a una estructura de [**\_ valores predeterminados de impresora**](printer-defaults.md) . Este valor puede ser **null**.

</dd> <dt>

*pOptions* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ Opciones de impresora**](printer-options.md) . Este valor puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

La versión ANSI de esta función no está implementada y devuelve un ERROR \_ no \_ admitido.

El parámetro *pDefault* le permite especificar el tipo de datos y los valores de modo de dispositivo que se usan para imprimir documentos enviados por la función [**StartDocPrinter**](startdocprinter.md) . Sin embargo, puede invalidar estos valores mediante la función [**SetJob**](setjob.md) después de haber iniciado un documento.

Puede llamar a la función **OpenPrinter2** para abrir un identificador a un servidor de impresión o para determinar los derechos de acceso de cliente a un servidor de impresión. Para ello, especifique el nombre del servidor de impresión en el parámetro *pPrinterName* , establezca los miembros **pDatatype** y **pDevMode** de la estructura [**de \_ valores predeterminados**](printer-defaults.md) de la impresora en **null** y establezca el miembro **DesiredAccess** para especificar un valor de máscara de acceso de servidor, como servidor \_ todos los \_ accesos. Cuando haya terminado con el identificador, páselo a la función [**ClosePrinter**](closeprinter.md) para cerrarlo.

Use el miembro **DesiredAccess** de la estructura de [**\_ valores predeterminados**](printer-defaults.md) de la impresora para especificar los derechos de acceso necesarios. Los derechos de acceso pueden ser uno de los siguientes.



| Valor de acceso deseado                        | Significado                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_administrar el acceso a las impresoras \_                 | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md).                                                                                                 |
| \_uso de acceso a impresoras \_                        | Para realizar operaciones de impresión básicas.                                                                                                                                                        |
| \_todo el \_ acceso a la impresora                        | Para realizar todas las tareas administrativas y las operaciones de impresión básicas excepto SINCRONIZAr. Consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights).                                         |
| \_acceso limitado de administración de acceso a impresoras \_ \_            | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md) y [**SetPrinterData**](setprinterdata.md). Este valor está disponible a partir de Windows 8.1. |
| valores de seguridad genéricos, como WRITE \_ DAC | Para permitir derechos de acceso de control específicos. Consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Si un usuario no tiene permiso para abrir una impresora o un servidor de impresión especificados con el acceso deseado, se producirá un error en la llamada a **OpenPrinter2** y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el valor error de \_ acceso \_ denegado.

Cuando *pPrinterName* es una impresora local, **OpenPrinter2** omite todos los valores de **dwFlags** a los que apunta la estructura de [**\_ Opciones de impresora**](printer-options.md) con *pOptions*, excepto el cambio de cliente de la opción de impresora \_ \_ \_ . Si se pasa el último, **OpenPrinter2** devolverá el error de \_ acceso \_ denegado. En consecuencia, al abrir una impresora local, **OpenPrinter2** no proporciona ninguna ventaja sobre [**OpenPrinter**](openprinter.md).

**Windows Vista:** Los datos de la impresora devueltos por **OpenPrinter2** se recuperan de una memoria caché local a menos que la **opción de impresora \_ \_ \_ no** esté establecida en el campo **dwFlags** de la estructura de [**\_ Opciones de impresora**](printer-options.md) a la que hace referencia *pOptions*.

## <a name="examples"></a>Ejemplos

En este ejemplo, **OpenPrinter2** produce un error cuando el \_ acceso a \_ la impresora Manage \_ Limited se pasa a la estructura de [**\_ valores predeterminados**](printer-defaults.md) de la impresora y el usuario no tiene el permiso adecuado.


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



Para obtener un programa de ejemplo que muestra cómo usar esta función, consulte [Cómo: imprimir mediante la API de impresión de GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
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

[**\_valores predeterminados de impresora**](printer-defaults.md)
</dt> <dt>

[**Opciones de impresora \_**](printer-options.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

