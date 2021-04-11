---
description: La función FindFirstPrinterChangeNotification crea un objeto de notificación de cambio y devuelve un identificador al objeto. Después, puede usar este identificador en una llamada a una de las funciones de espera para supervisar los cambios en la impresora o el servidor de impresión.
ms.assetid: 4155ef5c-cd96-4960-919b-d9a495bb73a5
title: Función FindFirstPrinterChangeNotification (winspool. h)
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
ms.openlocfilehash: 2da6a2ae73aa5b987ea3b8f8789f81ed0b4cdf06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276783"
---
# <a name="findfirstprinterchangenotification-function"></a>FindFirstPrinterChangeNotification función)

La función **FindFirstPrinterChangeNotification** crea un objeto de notificación de cambio y devuelve un identificador al objeto. Después, puede usar este identificador en una llamada a una de las funciones de espera para supervisar los cambios en la impresora o el servidor de impresión.

La llamada a **FindFirstPrinterChangeNotification** especifica el tipo de cambios que se van a supervisar. Puede especificar un conjunto de condiciones para supervisar los cambios, un conjunto de campos de información de la impresora que se van a supervisar o ambos.

Una operación de espera en el identificador de notificación de cambio se realiza correctamente cuando se produce uno de los cambios especificados en la impresora o el servidor de impresión especificado. A continuación, llame a la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para recuperar información sobre el cambio y restablecer el objeto de notificación de cambios para su uso en la siguiente operación de espera.

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora o del servidor de impresión que desea supervisar. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*fdwFilter* 
</dt> <dd>

Las condiciones que harán que el objeto de notificación de cambios entre en un estado señalado. Una notificación de cambio se produce cuando se cumplen una o varias de las condiciones especificadas. El parámetro *fdwFilter* puede ser cero si *PPrinterNotifyOptions* no es **null**.

Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CHANGE_FORM"></span><span id="printer_change_form"></span><dl> <dt>**\_formulario de cambio de impresora \_**</dt> </dl>                                   | Notifique cualquier cambio que se realice en un formulario. Puede establecer esta marca general o una o más de las siguientes marcas específicas:<br/> <dl> <dd>\_formulario para \_ Agregar y cambiar la impresora \_</dd> <dd>\_formulario de \_ conjunto de cambios de impresora \_</dd> <dd>\_formulario de \_ eliminación de cambio de impresora \_</dd> </dl>                                                                              |
| <span id="PRINTER_CHANGE_JOB"></span><span id="printer_change_job"></span><dl> <dt>**\_trabajo de cambio de impresora \_**</dt> </dl>                                      | Notifique cualquier cambio que se realice en un trabajo. Puede establecer esta marca general o una o más de las siguientes marcas específicas:<br/> <dl> <dd>\_ \_ Agregar trabajo de cambio de impresora \_</dd> <dd>\_trabajo de \_ conjunto de cambios de impresora \_</dd> <dd>\_trabajo de \_ eliminación de cambio de impresora \_</dd> <dd>\_trabajo de \_ escritura de cambio de impresora \_</dd> </dl>                                  |
| <span id="PRINTER_CHANGE_PORT"></span><span id="printer_change_port"></span><dl> <dt>**\_Puerto de cambio de impresora \_**</dt> </dl>                                   | Notifique cualquier cambio que se realice en un puerto. Puede establecer esta marca general o una o más de las siguientes marcas específicas:<br/> <dl> <dd>cambio de impresora- \_ \_ agregar \_ Puerto</dd> <dd>\_Puerto de \_ configuración de cambio de impresora \_ </dd> <dd>\_Puerto de \_ eliminación de cambio de impresora \_</dd> </dl>                                                                       |
| <span id="PRINTER_CHANGE_PRINT_PROCESSOR"></span><span id="printer_change_print_processor"></span><dl> <dt>**\_procesador de \_ impresión \_ cambiar impresora**</dt> </dl> | Notifique cualquier cambio en un procesador de impresión. Puede establecer esta marca general o una o más de las siguientes marcas específicas: <br/> <dl> <dd>cambio de impresora- \_ \_ agregar \_ procesador de impresión \_ </dd> <dd>cambio de impresora- \_ \_ eliminar \_ procesador de impresión \_</dd> </dl>                                                                                        |
| <span id="PRINTER_CHANGE_PRINTER"></span><span id="printer_change_printer"></span><dl> <dt>**\_impresora cambiar \_ impresora**</dt> </dl>                          | Notifique cualquier cambio en una impresora. Puede establecer esta marca general o una o más de las siguientes marcas específicas:<br/> <dl> <dd>cambio de impresora \_ \_ agregar \_ impresora</dd> <dd>\_impresora de \_ conjunto de cambios de impresora \_</dd> <dd>cambio de impresora- \_ \_ eliminar \_ impresora</dd> <dd>\_ \_ no se pudo cambiar la impresora \_ impresora de conexión \_</dd> </dl> |
| <span id="PRINTER_CHANGE_PRINTER_DRIVER"></span><span id="printer_change_printer_driver"></span><dl> <dt>**\_controlador de \_ impresora de cambio de impresora \_**</dt> </dl>    | Notifique cualquier cambio en un controlador de impresora. Puede establecer esta marca general o una o más de las siguientes marcas específicas:<br/> <dl> <dd>cambio de impresora- \_ \_ agregar \_ controlador de impresora \_</dd> <dd>\_controlador de \_ impresora de conjunto de cambios de impresora \_ \_</dd> <dd>\_controlador de \_ impresora para eliminar el cambio de impresora \_ \_</dd> </dl>                                   |
| <span id="PRINTER_CHANGE_ALL"></span><span id="printer_change_all"></span><dl> <dt>**\_cambiar \_ todo de impresora**</dt> </dl>                                      | Notificar si se produce alguno de los cambios anteriores.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**\_servidor de cambios de impresora \_**</dt> </dl>                             | Windows 7: notificar los cambios en el servidor.<br/> Esta marca no se incluye en los cambios supervisados mediante la configuración de la **impresora \_ cambiar \_ todos los** valores.<br/>                                                                                                                                                                                                      |



 

Para obtener descripciones de las marcas más específicas de la tabla anterior, vea la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .

</dd> <dt>

*fdwOptions* 
</dt> <dd>

Marca que determina la categoría de impresoras en las que funcionarán las notificaciones.



| Value                                                                                                                                                                                                                                                               | Significado                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_NOTIFY_CATEGORY_ALL"></span><span id="printer_notify_category_all"></span><dl> <dt>**Impresora \_ de NOTIFICACIÓN de \_ categoría \_ todos los**</dt> <dt>0x001000</dt> </dl> | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) devuelve notificaciones para impresoras 2D y 3D.<br/> |
| <span id="PRINTER_NOTIFY_CATEGORY_3D"></span><span id="printer_notify_category_3d"></span><dl> <dt>**Impresora \_ de Categoría de notificación en \_ \_ 3D**</dt> <dt>0x002000</dt> </dl>    | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) solo devuelve notificaciones para impresoras 3D.<br/>        |



 

Cuando esta marca se establece en cero (0), **FindFirstPrinterChangeNotification** solo funcionará para las impresoras 2D. Este es el valor predeterminado.

</dd> <dt>

*pPrinterNotifyOptions* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [**de \_ \_ Opciones de notificación de impresora**](printer-notify-options.md) . El miembro **pTypes** de esta estructura es una matriz de una o varias estructuras de tipo de opciones de notificación de [**impresora \_ \_ \_**](printer-notify-options-type.md) , cada una de las cuales especifica el campo de información de la impresora que se va a supervisar. Una notificación de cambio se produce cuando cambia uno o varios de los campos especificados. Cuando se produce un cambio, la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) puede recuperar la nueva información de la impresora. Este parámetro puede ser **null** si *fdwFilter* es distinto de cero.

Para obtener una lista de los campos que se pueden supervisar, vea [**tipo de opciones de notificación de impresora \_ \_ \_**](printer-notify-options-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un identificador de un objeto de notificación de cambio asociado a la impresora o servidor de impresión especificado.

Si se produce un error en la función, el valor devuelto es un valor de identificador no válido \_ \_ .

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Para supervisar una impresora o un servidor de impresión, llame a la función **FindFirstPrinterChangeNotification** y, a continuación, use el identificador de objeto de notificación de cambios devuelto en una llamada a una de las [funciones de espera](/windows/desktop/Sync/wait-functions). Una operación de espera en un objeto de notificación de cambios se cumple cuando el objeto de notificación de cambios entra en el estado señalado. El sistema señala el objeto cuando uno o varios de los cambios especificados por *fdwFilter* o *pPrinterNotifyOptions* se producen en la impresora supervisada o el servidor de impresión.

Cuando llame a **FindFirstPrinterChangeNotification**, *fdwFilter* debe ser distinto de cero o *pPrinterNotifyOptions* no debe ser **null**. Si se especifican ambos, las notificaciones se producirán para ambos.

Cuando se cumple una operación de espera en un objeto de notificación de cambio de impresora, llame a la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para determinar la causa de la notificación. En el caso de una condición especificada por *fdwFilter*, **FindNextPrinterChangeNotification** informa de la condición o condiciones que han cambiado. En el caso de un campo de información de impresora especificado por *pPrinterNotifyOptions*, **FindNextPrinterChangeNotification** notifica el campo o los campos que han cambiado, así como la nueva información de estos campos. **FindNextPrinterChangeNotification** también restablece el objeto de notificación de cambios en el estado no señalizado para que pueda usarlo en otra operación de espera para seguir supervisando la impresora o el servidor de impresión.

Con una excepción, no llame a la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) si el objeto de notificación de cambios no está en el estado señalado. Si la función wait devuelve el valor de \_ tiempo de espera de espera, el objeto de cambio no está en el estado señalado. Llame a la función **FindNextPrinterChangeNotification** solo si la función wait se realiza correctamente sin que se agote el tiempo de espera. La excepción es cuando se llama a **FindNextPrinterChangeNotification** con el \_ \_ bit de \_ actualización opciones de notificación de impresora establecido en el parámetro *pPrinterNotifyOptions* .

Cuando ya no necesite el objeto de notificación de cambios, ciérrelo llamando a la función [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .

Los autores de llamadas de **FindFirstPrinterChangeNotification** deben asegurarse de que el identificador de la impresora que se pasa a **FindFirstPrinterChangeNotification** sigue siendo válido hasta que se llame a [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) . Si el identificador de impresora está cerrado antes del identificador de notificación de cambio de impresora, no se entregarán más notificaciones.

**FindFirstPrinterChangeNotification** no enviará notificaciones de cambio para las impresoras 3D a los identificadores de servidor.

> [!Note]  
> En Windows XP con Service Pack 2 (SP2) y versiones posteriores, el Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se puede habilitar una excepción para compartir archivos e impresoras. Si un usuario realiza una conexión de impresora a otro equipo y la excepción no está habilitada, el usuario no recibirá las notificaciones de cambio de la impresora del servidor. Un administrador del equipo tendrá que habilitar la excepción.

 

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_Opciones de notificación de impresora \_**](printer-notify-options.md)
</dt> <dt>

[**\_tipo de \_ Opciones de notificación de impresora \_**](printer-notify-options-type.md)
</dt> </dl>

 

