---
description: La función FindNextPrinterChangeNotification recupera información sobre la notificación de cambios más reciente para un objeto de notificación de cambios asociado a una impresora o un servidor de impresión.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Función FindNextPrinterChangeNotification (winspool. h)
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
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910798"
---
# <a name="findnextprinterchangenotification-function"></a>FindNextPrinterChangeNotification función)

La función **FindNextPrinterChangeNotification** recupera información sobre la notificación de cambios más reciente para un objeto de notificación de cambios asociado a una impresora o un servidor de impresión. Llame a esta función cuando se satisfaga una operación de espera en el objeto de notificación de cambios.

La función también restablece el objeto de notificación de cambios al estado no señalado. Después, puede usar el objeto en otra operación de espera para seguir supervisando la impresora o el servidor de impresión. El sistema operativo establecerá el objeto en el estado señalado la próxima vez que se produzca uno de un conjunto de cambios especificado en la impresora o el servidor de impresión. La función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) crea el objeto de notificación de cambios y especifica el conjunto de cambios que se van a supervisar.

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

*hChange* \[ de\]
</dt> <dd>

Identificador de un objeto de notificación de cambios asociado a una impresora o servidor de impresión. Este identificador se obtiene mediante una llamada a la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . El sistema operativo establece este objeto de notificación de cambio en el estado señalado cuando detecta uno de los cambios especificados en el filtro de notificación de cambio del objeto.

</dd> <dt>

*pdwChange* \[ out, opcional\]
</dt> <dd>

Puntero a una variable cuyos bits se establecen para indicar los cambios que se produjeron para producir la notificación más reciente. Los marcadores de bits que se pueden establecer se corresponden con los especificados en el parámetro *fdwFilter* de la llamada a [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . El sistema establece una o varias de las siguientes marcas de bits.



| Value                                                                                                                                                                                                                                             | Significado                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**\_formulario para \_ Agregar y cambiar la impresora \_**</dt> </dl>                                                     | Se ha agregado un formulario al servidor.<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**\_ \_ Agregar trabajo de cambio de impresora \_**</dt> </dl>                                                        | Se envió un trabajo de impresión a la impresora.<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**cambio de impresora- \_ \_ agregar \_ Puerto**</dt> </dl>                                                     | Se ha agregado un puerto o un monitor al servidor.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**cambio de impresora- \_ \_ agregar \_ procesador de impresión \_**</dt> </dl>                   | Se ha agregado un procesador de impresión al servidor.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**cambio de impresora \_ \_ agregar \_ impresora**</dt> </dl>                                            | Se ha agregado una impresora al servidor.<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**cambio de impresora- \_ \_ agregar \_ controlador de impresora \_**</dt> </dl>                      | Se ha agregado un controlador de impresora al servidor.<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**\_Puerto de \_ configuración de cambio de impresora \_**</dt> </dl>                                   | Se configuró un puerto en el servidor.<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**\_formulario de \_ eliminación de cambio de impresora \_**</dt> </dl>                                            | Se eliminó un formulario del servidor.<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**\_trabajo de \_ eliminación de cambio de impresora \_**</dt> </dl>                                               | Se eliminó un trabajo.<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**\_Puerto de \_ eliminación de cambio de impresora \_**</dt> </dl>                                            | Se eliminó un puerto o un monitor del servidor.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**cambio de impresora- \_ \_ eliminar \_ procesador de impresión \_**</dt> </dl>          | Se eliminó un procesador de impresión del servidor.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**cambio de impresora- \_ \_ eliminar \_ impresora**</dt> </dl>                                   | Se eliminó una impresora.<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**\_controlador de \_ impresora para eliminar el cambio de impresora \_ \_**</dt> </dl>             | Se eliminó un controlador de impresora del servidor.<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**\_ \_ no se pudo cambiar la impresora \_ impresora de conexión \_**</dt> </dl> | Error en una conexión de impresora.<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**\_formulario de \_ conjunto de cambios de impresora \_**</dt> </dl>                                                     | Se estableció un formulario en el servidor.<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**\_trabajo de \_ conjunto de cambios de impresora \_**</dt> </dl>                                                        | Se estableció un trabajo.<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**\_impresora de \_ conjunto de cambios de impresora \_**</dt> </dl>                                            | Se estableció una impresora.<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**\_controlador de \_ impresora de conjunto de cambios de impresora \_ \_**</dt> </dl>                      | Se estableció un controlador de impresora.<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**\_trabajo de \_ escritura de cambio de impresora \_**</dt> </dl>                                                  | Se escribieron los datos del trabajo.<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**tiempo de espera de \_ cambio de impresora \_**</dt> </dl>                                                         | Se agotó el tiempo de espera del trabajo.<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**\_servidor de cambios de impresora \_**</dt> </dl>                                                            | Windows 7: se ha producido un cambio en el servidor.<br/>    |



 

</dd> <dt>

*pPrinterNotifyOptions* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [**de \_ \_ Opciones de notificación de impresora**](printer-notify-options.md) . Establezca el miembro **Flags** de esta estructura **en \_ Opciones de notificación de impresora \_ \_ Actualizar** para que la función devuelva los datos actuales de todos los campos supervisados de información de la impresora. La función omite todos los demás miembros de la estructura. Este parámetro puede ser **NULL**.

</dd> <dt>

*ppPrinterNotifyInfo* \[ out, opcional\]
</dt> <dd>

Puntero a una variable de puntero que recibe un puntero a un búfer asignado por el sistema y de solo lectura. Llame a la función [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) para liberar el búfer cuando termine de usarlo. Este parámetro puede ser **null** si no se requiere información.

El búfer contiene una estructura de [**\_ \_ información de notificación de impresora**](printer-notify-info.md) , que contiene una matriz de estructuras de [**\_ \_ \_ datos de información de notificación de impresora**](printer-notify-info-data.md) . Cada elemento de la matriz contiene información sobre uno de los campos especificados en el parámetro *pPrinterNotifyOptions* de la llamada a [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . Normalmente, la función solo proporciona datos para los campos que han cambiado para generar la notificación más reciente. Sin embargo, si la estructura a la que apunta el parámetro *pPrinterNotifyOptions* especifica la **\_ \_ \_ actualización de las opciones de notificación** de la impresora, la función proporciona datos para todos los campos supervisados.

Si el **bit \_ \_ \_ descartado** de la información de notificación de impresora se establece en el miembro de **marcas** de la estructura de [**\_ \_ información de notificación**](printer-notify-info.md) de la impresora, se ha producido un desbordamiento o un error, y es posible que se hayan perdido las notificaciones. En este caso, no se enviarán notificaciones adicionales hasta que realice una segunda llamada a **FindNextPrinterChangeNotification** que especifique la **\_ \_ \_ actualización de las opciones de notificación** de la impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Llame a la función **FindNextPrinterChangeNotification** después de que se haya satisfecho una operación de espera en un objeto de notificación creado por [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . La llamada a **FindNextPrinterChangeNotification** permite obtener información sobre el cambio que cumplía la operación de espera y restablece el objeto de notificación para que se pueda señalizar cuando se produzca el siguiente cambio.

Con una excepción, no llame a la función **FindNextPrinterChangeNotification** si el objeto de notificación de cambios no está en el estado señalado. Si una función wait devuelve el valor **de \_ tiempo de espera** de la espera, el objeto de cambio no está en el estado señalado. Llame a la función **FindNextPrinterChangeNotification** solo si la función wait se realiza correctamente sin que se agote el tiempo de espera. La excepción es cuando se llama a **FindNextPrinterChangeNotification** con el bit de **\_ \_ \_ actualización opciones de notificación de impresora** establecido en el parámetro *pPrinterNotifyOptions* . Tenga en cuenta que incluso cuando se establece esta marca, sigue siendo posible establecer la marca de notificación de la **\_ \_ información \_ de notificaciones** de la impresora en el parámetro *ppPrinterNotifyInfo* .

Para seguir supervisando los cambios en la impresora o el servidor de impresión, repita el ciclo de llamada a una de las [funciones de espera](/windows/desktop/Sync/wait-functions) y, a continuación, llame a la función **FindNextPrinterChangeNotification** para examinar el cambio y restablecer el objeto de notificación.

**FindNextPrinterChangeNotification** puede combinar varios cambios en el mismo campo de información de la impresora en una sola notificación. Cuando esto ocurre, la función suele contraer todos los cambios del campo en una única entrada en la matriz de estructuras de [**\_ \_ \_ datos de notificación**](printer-notify-info-data.md) de la impresora en *ppPrinterNotifyInfo*; la única entrada solo informa de la información más reciente. Sin embargo, para algunos campos de información de trabajos e impresoras, la función puede devolver varias entradas de matriz para el mismo campo. En este caso, la última entrada de la matriz para el campo informa de los datos actuales y las entradas anteriores contienen los datos de las fases intermedias.

Cuando ya no necesite el objeto de notificación de cambios, ciérrelo llamando a la función [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .

> [!Note]  
> En Windows XP con Service Pack 2 (SP2) y versiones posteriores, el Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se puede habilitar una excepción para compartir archivos e impresoras. Si un usuario realiza una conexión de impresora a otro equipo y la excepción no está habilitada, el usuario no recibirá las notificaciones de cambio de la impresora del servidor. Un administrador del equipo tendrá que habilitar la excepción.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo se puede supervisar el estado de la impresora mediante estas funciones.


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
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
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

[**\_información de notificación de impresora \_**](printer-notify-info.md)
</dt> <dt>

[**\_datos de \_ información de notificación de impresora \_**](printer-notify-info-data.md)
</dt> <dt>

[**\_Opciones de notificación de impresora \_**](printer-notify-options.md)
</dt> </dl>

 

