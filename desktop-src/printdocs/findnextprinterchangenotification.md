---
description: La función FindNextPrinterChangeNotification recupera información sobre la notificación de cambios más reciente para un objeto de notificación de cambios asociado a una impresora o servidor de impresión.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Función FindNextPrinterChangeNotification (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 37b05603a75f7bc8e68ead2d0dffdec2e99e7618e5461360760f2d9c89ae52da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112485"
---
# <a name="findnextprinterchangenotification-function"></a>Función FindNextPrinterChangeNotification

La **función FindNextPrinterChangeNotification** recupera información sobre la notificación de cambios más reciente para un objeto de notificación de cambios asociado a una impresora o servidor de impresión. Llame a esta función cuando se cumple una operación de espera en el objeto de notificación de cambios.

La función también restablece el objeto de notificación de cambios al estado no señalado. A continuación, puede usar el objeto en otra operación de espera para seguir supervisando la impresora o el servidor de impresión. El sistema operativo establecerá el objeto en el estado señalado la próxima vez que se produzca uno de los cambios especificados en la impresora o el servidor de impresión. La [**función FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) crea el objeto de notificación de cambios y especifica el conjunto de cambios que se supervisarán.

## <a name="syntax"></a>Sintaxis


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hChange* \[ En\]
</dt> <dd>

Identificador de un objeto de notificación de cambios asociado a una impresora o servidor de impresión. Para obtener este tipo de identificador, llame a [**la función FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) El sistema operativo establece este objeto de notificación de cambios en el estado señalado cuando detecta uno de los cambios especificados en el filtro de notificación de cambios del objeto.

</dd> <dt>

*pdwChange* \[ out, opcional\]
</dt> <dd>

Puntero a una variable cuyos bits se establecen para indicar los cambios que se produjeron para provocar la notificación más reciente. Las marcas de bits que se pueden establecer corresponden a las especificadas en el parámetro *fdwFilter* de la llamada [**FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) El sistema establece uno o varios de los siguientes marcadores de bits.



| Value                                                                                                                                                                                                                                             | Significado                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**AGREGAR \_ FORMULARIO DE CAMBIO DE \_ \_ IMPRESORA**</dt> </dl>                                                     | Se ha agregado un formulario al servidor.<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**AGREGAR \_ TRABAJO DE CAMBIO DE \_ \_ IMPRESORA**</dt> </dl>                                                        | Se envió un trabajo de impresión a la impresora.<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**CAMBIO \_ DE IMPRESORA AGREGAR \_ \_ PUERTO**</dt> </dl>                                                     | Se ha agregado un puerto o monitor al servidor.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**CAMBIO \_ DE IMPRESORA AGREGAR PROCESADOR DE \_ \_ \_ IMPRESIÓN**</dt> </dl>                   | Se agregó un procesador de impresión al servidor.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**CAMBIO \_ DE IMPRESORA AGREGAR \_ \_ IMPRESORA**</dt> </dl>                                            | Se agregó una impresora al servidor.<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**CAMBIO \_ DE IMPRESORA AGREGAR CONTROLADOR DE \_ \_ \_ IMPRESORA**</dt> </dl>                      | Se agregó un controlador de impresora al servidor.<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**CAMBIO DE \_ IMPRESORA \_ CONFIGURAR \_ PUERTO**</dt> </dl>                                   | Se configuró un puerto en el servidor.<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**FORMULARIO \_ DE ELIMINACIÓN \_ DE CAMBIOS DE \_ IMPRESORA**</dt> </dl>                                            | Se eliminó un formulario del servidor.<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**TRABAJO DE \_ ELIMINACIÓN \_ DE CAMBIO DE \_ IMPRESORA**</dt> </dl>                                               | Se eliminó un trabajo.<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**CAMBIO \_ DE IMPRESORA ELIMINAR \_ \_ PUERTO**</dt> </dl>                                            | Se eliminó un puerto o un monitor del servidor.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**CAMBIO \_ DE IMPRESORA ELIMINAR PROCESADOR DE \_ \_ \_ IMPRESIÓN**</dt> </dl>          | Se eliminó un procesador de impresión del servidor.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**CAMBIO \_ DE IMPRESORA ELIMINAR \_ \_ IMPRESORA**</dt> </dl>                                   | Se eliminó una impresora.<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**CAMBIO \_ DE IMPRESORA ELIMINAR CONTROLADOR DE \_ \_ \_ IMPRESORA**</dt> </dl>             | Se eliminó un controlador de impresora del servidor.<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**ERROR EN \_ LA IMPRESORA AL CAMBIAR LA CONEXIÓN DE LA \_ \_ \_ IMPRESORA**</dt> </dl> | Error en la conexión de una impresora.<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**FORMULARIO DE \_ CONJUNTO DE CAMBIOS DE \_ \_ IMPRESORA**</dt> </dl>                                                     | Se estableció un formulario en el servidor.<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**TRABAJO DE \_ CONJUNTO DE CAMBIOS DE \_ \_ IMPRESORA**</dt> </dl>                                                        | Se estableció un trabajo.<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**IMPRESORA DE \_ CONJUNTO DE CAMBIOS DE \_ \_ IMPRESORA**</dt> </dl>                                            | Se estableció una impresora.<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**CONTROLADOR DE \_ IMPRESORA DEL CONJUNTO DE CAMBIOS DE \_ \_ \_ IMPRESORA**</dt> </dl>                      | Se estableció un controlador de impresora.<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**TRABAJO DE \_ ESCRITURA DE CAMBIO DE \_ \_ IMPRESORA**</dt> </dl>                                                  | Se escribieron los datos del trabajo.<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**TIEMPO DE ESPERA \_ DE CAMBIO \_ DE IMPRESORA**</dt> </dl>                                                         | Se ha producido un tiempo de espera del trabajo.<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**SERVIDOR DE \_ CAMBIOS DE \_ IMPRESORA**</dt> </dl>                                                            | Windows 7: Se ha producido un cambio en el servidor.<br/>    |



 

</dd> <dt>

*pPrinterNotifyOptions* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [**PRINTER \_ NOTIFY \_ OPTIONS.**](printer-notify-options.md) Establezca el **miembro Flags** de esta estructura en **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH** para que la función devuelva los datos actuales de todos los campos de información de impresora supervisados. La función omite todos los demás miembros de la estructura . Este parámetro puede ser **NULL**.

</dd> <dt>

*ppPrinterNotifyInfo* \[ out, opcional\]
</dt> <dd>

Puntero a una variable de puntero que recibe un puntero a un búfer de solo lectura asignado por el sistema. Llame a [**la función FreePrinterNotifyInfo**](freeprinternotifyinfo.md) para liberar el búfer cuando haya terminado con él. Este parámetro puede ser **NULL** si no se requiere ninguna información.

El búfer contiene una estructura [**PRINTER \_ NOTIFY \_ INFO,**](printer-notify-info.md) que contiene una matriz de [**estructuras PRINTER NOTIFY INFO \_ \_ \_ DATA.**](printer-notify-info-data.md) Cada elemento de la matriz contiene información sobre uno de los campos especificados en el parámetro *pPrinterNotifyOptions* de la llamada [**FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) Normalmente, la función proporciona datos solo para los campos que cambiaron para provocar la notificación más reciente. Sin embargo, si la estructura a la que apunta el parámetro *pPrinterNotifyOptions* especifica **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH**, la función proporciona datos para todos los campos supervisados.

Si el bit **PRINTER \_ NOTIFY INFO \_ \_ DISCARDED** está establecido en el miembro **Flags** de la estructura [**PRINTER NOTIFY \_ \_ INFO,**](printer-notify-info.md) se ha producido un desbordamiento o un error, y es posible que se hayan perdido las notificaciones. En este caso, no se enviará ninguna notificación adicional hasta que realice una segunda llamada **FindNextPrinterChangeNotification** que especifique **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Llame a **la función FindNextPrinterChangeNotification después** de que se haya satisfecho una operación de espera en un objeto de notificación creado por [**FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) Llamar **a FindNextPrinterChangeNotification** le permite obtener información sobre el cambio que satisface la operación de espera y restablece el objeto de notificación para que se pueda señalar cuando se produzca el siguiente cambio.

Con una excepción, no llame a la función **FindNextPrinterChangeNotification** si el objeto de notificación de cambios no está en el estado señalado. Si una función wait devuelve el valor **WAIT \_ TIMEOUT**, el objeto de cambio no está en el estado señalado. Llame a **la función FindNextPrinterChangeNotification** solo si la función wait se realiza correctamente sin tiempo de espera. La excepción es cuando se llama a **FindNextPrinterChangeNotification** con el bit **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH** establecido en el *parámetro pPrinterNotifyOptions.* Tenga en cuenta que incluso cuando se establece esta marca, todavía es posible establecer la marca **PRINTER \_ NOTIFY INFO \_ \_ DISCARDED** en el *parámetro ppPrinterNotifyInfo.*

Para seguir supervisando la impresora o el servidor de [](/windows/desktop/Sync/wait-functions) impresión en busca de cambios, repita el ciclo de llamada a una de las funciones de espera y, a continuación, llame a la función **FindNextPrinterChangeNotification** para examinar el cambio y restablecer el objeto de notificación.

**FindNextPrinterChangeNotification puede** combinar varios cambios en el mismo campo de información de impresora en una única notificación. Cuando esto sucede, la función normalmente contrae todos los cambios del campo en una sola entrada de la matriz de estructuras [**PRINTER \_ NOTIFY INFO \_ \_ DATA**](printer-notify-info-data.md) en *ppPrinterNotifyInfo;* la entrada única solo notifica la información más reciente. Sin embargo, para algunos campos de información de trabajo e impresora, la función puede devolver varias entradas de matriz para el mismo campo. En este caso, la última entrada de matriz para el campo notifica los datos actuales y las entradas anteriores contienen los datos de las fases intermedias.

Cuando ya no necesite el objeto de notificación de cambios, cierre el objeto llamando a la [**función FindClosePrinterChangeNotification.**](findcloseprinterchangenotification.md)

> [!Note]  
> En Windows XP con Service Pack 2 (SP2) y versiones posteriores, el Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se puede habilitar una excepción para el uso compartido de archivos e impresión. Si un usuario realiza una conexión de impresora a otra máquina y la excepción no está habilitada, el usuario no recibirá notificaciones de cambio de impresora del servidor. Un administrador de equipo tendrá que habilitar la excepción.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo puede supervisar el estado de la impresora mediante estas funciones.


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**INFORMACIÓN DE \_ NOTIFICACIÓN DE \_ IMPRESORA**](printer-notify-info.md)
</dt> <dt>

[**DATOS DE \_ INFORMACIÓN DE NOTIFICACIÓN DE \_ \_ IMPRESORA**](printer-notify-info-data.md)
</dt> <dt>

[**OPCIONES DE \_ NOTIFICACIÓN DE \_ IMPRESORA**](printer-notify-options.md)
</dt> </dl>

 

