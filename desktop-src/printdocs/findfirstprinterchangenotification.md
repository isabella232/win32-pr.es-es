---
description: La función FindFirstPrinterChangeNotification crea un objeto de notificación de cambios y devuelve un identificador al objeto . A continuación, puede usar este identificador en una llamada a una de las funciones de espera para supervisar los cambios en la impresora o el servidor de impresión.
ms.assetid: 4155ef5c-cd96-4960-919b-d9a495bb73a5
title: Función FindFirstPrinterChangeNotification (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindFirstPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 679d0bfe4b87f934f223ad83f1fd1ee341b5ce891736727a4faa537d782d3687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971534"
---
# <a name="findfirstprinterchangenotification-function"></a>Función FindFirstPrinterChangeNotification

La **función FindFirstPrinterChangeNotification** crea un objeto de notificación de cambios y devuelve un identificador al objeto . A continuación, puede usar este identificador en una llamada a una de las funciones de espera para supervisar los cambios en la impresora o el servidor de impresión.

La **llamada a FindFirstPrinterChangeNotification** especifica el tipo de cambios que se supervisarán. Puede especificar un conjunto de condiciones para supervisar los cambios, un conjunto de campos de información de impresora para supervisar o ambos.

Una operación de espera en el identificador de notificación de cambios se realiza correctamente cuando se produce uno de los cambios especificados en la impresora o el servidor de impresión especificados. A continuación, llame a la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para recuperar información sobre el cambio y restablecer el objeto de notificación de cambios para usarlo en la siguiente operación de espera.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE FindFirstPrinterChangeNotification(
  _In_     HANDLE hPrinter,
           DWORD  fdwFilter,
           DWORD  fdwOptions,
  _In_opt_ LPVOID pPrinterNotifyOptions
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador para la impresora o el servidor de impresión que desea supervisar. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*fdwFilter* 
</dt> <dd>

Condiciones que harán que el objeto de notificación de cambios entre en un estado señalado. Una notificación de cambio se produce cuando se cumplen una o varias de las condiciones especificadas. El *parámetro fdwFilter* puede ser cero si *pPrinterNotifyOptions* no es **NULL.**

Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CHANGE_FORM"></span><span id="printer_change_form"></span><dl> <dt>**FORMULARIO DE \_ CAMBIO DE \_ IMPRESORA**</dt> </dl>                                   | Notificar los cambios realizados en un formulario. Puede establecer esta marca general o una o varias de las siguientes marcas específicas:<br/> <dl> <dd>AGREGAR \_ FORMULARIO DE CAMBIO DE \_ \_ IMPRESORA</dd> <dd>FORMULARIO DE \_ CONJUNTO DE CAMBIOS DE \_ \_ IMPRESORA</dd> <dd>FORMULARIO \_ DE ELIMINACIÓN \_ DE CAMBIOS DE \_ IMPRESORA</dd> </dl>                                                                              |
| <span id="PRINTER_CHANGE_JOB"></span><span id="printer_change_job"></span><dl> <dt>**TRABAJO DE \_ CAMBIO DE \_ IMPRESORA**</dt> </dl>                                      | Notificar los cambios realizados en un trabajo. Puede establecer esta marca general o una o varias de las siguientes marcas específicas:<br/> <dl> <dd>AGREGAR \_ TRABAJO DE CAMBIO DE \_ \_ IMPRESORA</dd> <dd>TRABAJO DE \_ CONJUNTO DE CAMBIOS DE \_ \_ IMPRESORA</dd> <dd>TRABAJO DE \_ ELIMINACIÓN \_ DE CAMBIO DE \_ IMPRESORA</dd> <dd>TRABAJO DE \_ ESCRITURA DE CAMBIO DE \_ \_ IMPRESORA</dd> </dl>                                  |
| <span id="PRINTER_CHANGE_PORT"></span><span id="printer_change_port"></span><dl> <dt>**PUERTO DE \_ CAMBIO DE \_ IMPRESORA**</dt> </dl>                                   | Notificar los cambios realizados en un puerto. Puede establecer esta marca general o una o varias de las siguientes marcas específicas:<br/> <dl> <dd>CAMBIO \_ DE IMPRESORA AGREGAR \_ \_ PUERTO</dd> <dd>CAMBIO DE \_ IMPRESORA \_ CONFIGURAR \_ PUERTO </dd> <dd>CAMBIO DE \_ IMPRESORA \_ ELIMINAR \_ PUERTO</dd> </dl>                                                                       |
| <span id="PRINTER_CHANGE_PRINT_PROCESSOR"></span><span id="printer_change_print_processor"></span><dl> <dt>**PROCESADOR DE \_ IMPRESIÓN DE CAMBIO DE \_ \_ IMPRESORA**</dt> </dl> | Notificar cualquier cambio en un procesador de impresión. Puede establecer esta marca general o una o varias de las siguientes marcas específicas: <br/> <dl> <dd>CAMBIO \_ DE IMPRESORA AGREGAR PROCESADOR DE \_ \_ \_ IMPRESIÓN </dd> <dd>CAMBIO \_ DE IMPRESORA ELIMINAR PROCESADOR DE \_ \_ \_ IMPRESIÓN</dd> </dl>                                                                                        |
| <span id="PRINTER_CHANGE_PRINTER"></span><span id="printer_change_printer"></span><dl> <dt>**IMPRESORA \_ DE CAMBIO DE \_ IMPRESORA**</dt> </dl>                          | Notifique los cambios en una impresora. Puede establecer esta marca general o una o varias de las siguientes marcas específicas:<br/> <dl> <dd>CAMBIO \_ DE IMPRESORA AGREGAR \_ \_ IMPRESORA</dd> <dd>IMPRESORA DE \_ CONJUNTO DE CAMBIOS DE \_ \_ IMPRESORA</dd> <dd>CAMBIO \_ DE IMPRESORA ELIMINAR \_ \_ IMPRESORA</dd> <dd>ERROR EN \_ LA IMPRESORA AL CAMBIAR LA CONEXIÓN DE LA \_ \_ \_ IMPRESORA</dd> </dl> |
| <span id="PRINTER_CHANGE_PRINTER_DRIVER"></span><span id="printer_change_printer_driver"></span><dl> <dt>**CONTROLADOR DE \_ IMPRESORA DE CAMBIO DE \_ \_ IMPRESORA**</dt> </dl>    | Notificar cualquier cambio en un controlador de impresora. Puede establecer esta marca general o una o varias de las siguientes marcas específicas:<br/> <dl> <dd>CAMBIO \_ DE IMPRESORA AGREGAR CONTROLADOR DE \_ \_ \_ IMPRESORA</dd> <dd>CONTROLADOR DE \_ IMPRESORA DEL CONJUNTO DE CAMBIOS DE \_ \_ \_ IMPRESORA</dd> <dd>CAMBIO \_ DE IMPRESORA ELIMINAR CONTROLADOR DE \_ \_ \_ IMPRESORA</dd> </dl>                                   |
| <span id="PRINTER_CHANGE_ALL"></span><span id="printer_change_all"></span><dl> <dt>**IMPRESORA \_ CAMBIAR \_ TODO**</dt> </dl>                                      | Notifique si se produce alguno de los cambios anteriores.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**SERVIDOR DE \_ CAMBIOS DE \_ IMPRESORA**</dt> </dl>                             | Windows 7: notificar cualquier cambio en el servidor.<br/> Esta marca no se incluye en los cambios supervisados estableciendo el valor **PRINTER \_ CHANGE \_ ALL.**<br/>                                                                                                                                                                                                      |



 

Para obtener descripciones de las marcas más específicas de la tabla anterior, vea la función [**FindNextPrinterChangeNotification.**](findnextprinterchangenotification.md)

</dd> <dt>

*fdwOptions* 
</dt> <dd>

Marca que determina la categoría de impresoras para las que funcionarán las notificaciones.



| Value                                                                                                                                                                                                                                                               | Significado                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_NOTIFY_CATEGORY_ALL"></span><span id="printer_notify_category_all"></span><dl> <dt>**IMPRESORA \_ NOTIFICAR \_ A LA CATEGORÍA \_ TODOS**</dt> <dt>los 0x001000</dt> </dl> | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) devuelve notificaciones para impresoras 2D y 3D.<br/> |
| <span id="PRINTER_NOTIFY_CATEGORY_3D"></span><span id="printer_notify_category_3d"></span><dl> <dt>**IMPRESORA \_ NOTIFICACIÓN \_ A LA CATEGORÍA \_ 3D**</dt> <dt>0x002000</dt> </dl>    | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) devuelve notificaciones solo para impresoras 3D.<br/>        |



 

Cuando esta marca se establece en cero (0), **FindFirstPrinterChangeNotification** solo funcionará para impresoras 2D. Este es el valor predeterminado.

</dd> <dt>

*pPrinterNotifyOptions* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [**PRINTER \_ NOTIFY \_ OPTIONS.**](printer-notify-options.md) El **miembro pTypes** de esta estructura es una matriz de una o varias estructuras [**PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE,**](printer-notify-options-type.md) cada una de las cuales especifica un campo de información de impresora que se va a supervisar. Se produce una notificación de cambio cuando cambia uno o varios de los campos especificados. Cuando se produce un cambio, la [**función FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) puede recuperar la información de la nueva impresora. Este parámetro puede ser **NULL** si *fdwFilter* es distinto de cero.

Para obtener una lista de los campos que se pueden supervisar, vea [**PRINTER \_ NOTIFY OPTIONS \_ \_ TYPE**](printer-notify-options-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador de un objeto de notificación de cambios asociado con la impresora o el servidor de impresión especificados.

Si se produce un error en la función, el valor devuelto es INVALID \_ HANDLE \_ VALUE.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Para supervisar una impresora o un servidor de impresión, llame a la función **FindFirstPrinterChangeNotification** y, a continuación, use el identificador de objeto de notificación de cambios devuelto en una llamada a una de las [funciones de espera](/windows/desktop/Sync/wait-functions). Se satisface una operación de espera en un objeto de notificación de cambios cuando el objeto de notificación de cambios entra en el estado señalado. El sistema señala el objeto cuando uno o varios de los cambios especificados por *fdwFilter* o *pPrinterNotifyOptions* se producen en la impresora supervisada o el servidor de impresión.

Al llamar a **FindFirstPrinterChangeNotification**, *fdwFilter* debe ser distinto de cero o *pPrinterNotifyOptions* debe ser distinto de **NULL.** Si se especifican ambos, se producirán notificaciones para ambos.

Cuando se cumple una operación de espera en un objeto de notificación de cambio de impresora, llame a la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para determinar la causa de la notificación. Para una condición especificada por *fdwFilter,* **FindNextPrinterChangeNotification** notifica la condición o condiciones que han cambiado. Para un campo de información de impresora especificado por *pPrinterNotifyOptions,* **FindNextPrinterChangeNotification** notifica el campo o los campos que han cambiado, así como la nueva información de estos campos. **FindNextPrinterChangeNotification** también restablece el objeto de notificación de cambios al estado no firmado para que pueda usarlo en otra operación de espera para seguir supervisando la impresora o el servidor de impresión.

Con una excepción, no llame a la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) si el objeto de notificación de cambios no está en el estado señalado. Si la función wait devuelve el valor WAIT TIMEOUT, el objeto de cambio \_ no está en el estado señalado. Llame a **la función FindNextPrinterChangeNotification** solo si la función wait se realiza correctamente sin tiempo de espera. La excepción es cuando se llama a **FindNextPrinterChangeNotification** con el bit PRINTER NOTIFY OPTIONS REFRESH establecido en el \_ \_ parámetro \_ *pPrinterNotifyOptions.*

Cuando ya no necesite el objeto de notificación de cambios, cierre el objeto llamando a la [**función FindClosePrinterChangeNotification.**](findcloseprinterchangenotification.md)

Los llamadores de **FindFirstPrinterChangeNotification** deben asegurarse de que el identificador de impresora pasado a **FindFirstPrinterChangeNotification** siga siendo válido hasta que se llame a [**FindClosePrinterChangeNotification.**](findcloseprinterchangenotification.md) Si el identificador de impresora se cierra antes del identificador de notificación de cambio de impresora, no se podrán entregar más notificaciones.

**FindFirstPrinterChangeNotification** no enviará notificaciones de cambios para impresoras 3D a identificadores de servidor.

> [!Note]  
> En Windows XP con Service Pack 2 (SP2) y versiones posteriores, el Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se puede habilitar una excepción para el uso compartido de archivos e impresión. Si un usuario realiza una conexión de impresora a otra máquina y la excepción no está habilitada, el usuario no recibirá notificaciones de cambio de impresora del servidor. Un administrador de equipo tendrá que habilitar la excepción.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**OPCIONES DE \_ NOTIFICACIÓN DE \_ IMPRESORA**](printer-notify-options.md)
</dt> <dt>

[**TIPO DE \_ OPCIONES DE NOTIFICACIÓN DE \_ \_ IMPRESORA**](printer-notify-options-type.md)
</dt> </dl>

 

