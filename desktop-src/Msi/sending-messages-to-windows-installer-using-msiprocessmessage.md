---
description: Los mensajes enviados mediante MsiProcessMessage son los mismos mensajes que recibe la función de devolución de llamada INSTALLUI HANDLER si se llamó \_ a MsiSetExternalUI.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Enviar mensajes al instalador Windows mediante MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260967"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a>Envío de mensajes Windows instalador mediante MsiProcessMessage

Los mensajes enviados mediante [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) son los mismos mensajes que recibe la función de devolución de llamada [**INSTALLUI \_ HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera) si se llamó a [**MsiSetExternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) De lo contrario, Windows Installer controla los mensajes. Para obtener más información, vea [Analizar Windows mensajes del instalador.](parsing-windows-installer-messages.md)

Por ejemplo, para enviar un mensaje DE ERROR INSTALLMESSAGE con el icono MB ICONWARNING y los botones \_ \_ MB \_ ABORTRETRYCANCEL:


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



Donde *hInstall* es el identificador de la instalación, proporcionado a una acción personalizada o al identificador *hProduct* de [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) o [**MsiOpenPackage,**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) *y hRec* es el registro que contiene la información de error que se va a dar formato. Para obtener información sobre cómo se realiza el formato, [**vea MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).

De forma predeterminada, si se envía un mensaje INSTALLMESSAGE ERROR o INSTALLMESSAGE FATALEXIT sin especificar el tipo de botón o los tipos de icono, se usa MB OK, no icon y \_ \_ MB \_ \_ DEFBUTTON1.

Windows El instalador no etiqueta el **botón ABORT** con la cadena "Abort" al mostrar un cuadro de mensajes con la especificación del botón MB ABORTRETRYIGNORE, sino que etiqueta el botón con la cadena \_ "Cancel". Todos los mensajes de error evitan usar la palabra "Abort" y, en su lugar, usan la palabra "Cancel".

El *parámetro hRecord* de la [**función MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) depende del tipo de mensaje enviado a [**MsiProcessMessage.**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) En la lista siguiente se detallan los requisitos del registro en relación con el tipo de mensaje:

INSTALLMESSAGE \_ FATALEXIT

 

INFORMACIÓN DE \_ INSTALLMESSAGE

 

INSTALLMESSAGE \_ OUTOFDISKSPACE



| Campo         | Descripción                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Plantilla para el formato de la cadena resultante. Consulte [**MsiFormatRecord para**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) obtener más información. Se hace referencia a los campos del registro mediante \[ 1 \] para el campo 1, \[ 2 para el campo \] 2, etc. |
| De 1 a *n* | Todos los campos subsiguientes están directamente relacionados con los campos a los que hace referencia la plantilla en el campo 0.                                                                                                                    |



 

Si el campo 0 es NULL, la cadena recibida por el controlador de interfaz de usuario tiene el formato: 1: datos del campo 1 2: datos del campo 2, lo que significa que para cada campo del registro, la cadena contiene el número de campo seguido de los datos almacenados en el \[ \] \[ \] campo.

Los mensajes de información de [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) se registran cuando [](command-line-options.md) [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) [](logging.md) , la opción de línea de comandos "/l" o la directiva de registro especifican "I" o INSTALLLOGMODE \_ INFO.

ERROR \_ DE INSTALLMESSAGE

 

ADVERTENCIA DE \_ INSTALLMESSAGE

 

INSTALLMESSAGE \_ USER

Para usar un mensaje de la tabla Error.



| Campo         | Descripción                                           |
|---------------|-------------------------------------------------------|
| 0             | Debe ser NULL.                                         |
| 1             | Número de mensaje en la [tabla error](error-table.md). |
| De 2 a *n* | Relacionado con el mensaje especificado en la tabla Error.  |



 

Por ejemplo.



| Campo | Tipo   | Datos       |
|-------|--------|------------|
| 0     | string | null       |
| 1     | int    | 1304       |
| 2     | string | Myfile.txt |



 

El mensaje resultante recibido del controlador de interfaz de usuario es:

Error 1304. Error al escribir en el archivo: Myfile.txt. Compruebe que tiene acceso a ese directorio.

Si el campo 0 no es NULL, se invalida el mensaje de la tabla de errores. En su lugar, la plantilla de campo 0 determina el formato del mensaje.

El mensaje también puede especificar los botones, incluido el botón predeterminado, y el icono para usarlo con el mensaje como se mencionó anteriormente. Los tipos de botón e icono se enumeran en [**INSTALLUI \_ HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera).

INSTALLMESSAGE \_ COMMONDATA

Este mensaje se envía para habilitar o deshabilitar el botón **Cancelar** en un cuadro de diálogo de progreso.



| Campo | Descripción                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Sin usar.                                                                                                                                      |
| 1     | 2 hace referencia al **botón** Cancelar.                                                                                                           |
| 2     | Un valor de 1 indica que el **botón Cancelar** debe estar visible. Un valor de 0 indica que el **botón Cancelar** debe ser invisible.<br/> |



 

Por ejemplo, para deshabilitar u ocultar el **botón Cancelar,** el registro aparecería como sigue.



| Campo | Tipo   | Datos |
|-------|--------|------|
| 0     | string | null |
| 1     | int    | 2    |
| 2     | int    | 0    |



 

INSTALLMESSAGE \_ ACTIONSTART

 

INSTALLMESSAGE \_ ACTIONDATA

El registro INSTALLMESSAGE \_ ACTIONSTART determina el formato del registro ActionData.



| Campo | Descripción                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| 0     | null                                                                                                          |
| 1     | Nombre de la acción. El nombre de este campo debe ser distinto de NULL.                                                         |
| 2     | Descripción de la acción.                                                                                           |
| 3     | Plantilla de acción. Se usa para ActionData cuyo mensaje se está formatendo según esta plantilla. |



 

No haga referencia al campo 0 en el mensaje de plantilla Acción.

El registro INSTALLMESSAGE \_ ACTIONDATA tiene el formato siguiente.



| Campo         | Descripción                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | null                                                                                                                                               |
| De 1 a *n* | Depende del campo 3 del mensaje o plantilla INSTALLMESSAGE ACTIONSTART correspondiente \_ especificado en la tabla [ActionText](actiontext-table.md). |



 

Por ejemplo, el registro INSTALLMESSAGE \_ ACTIONSTART.



| Campo | Tipo   | Datos                                                            |
|-------|--------|-----------------------------------------------------------------|
| 0     | string | null                                                            |
| 1     | string | MyAction                                                        |
| 2     | string | Esta es la descripción de "MyAction".                           |
| 3     | string | Plantilla myAction: los datos field1 son \[ \] 1. Los datos del campo 2 son \[ \] 2. |



 

La plantilla de INSTALLMESSAGE ACTIONSTART (campo 3) hace referencia a los campos 1 y 2; el registro INSTALLMESSAGE ACTIONDATA debe tener 2 campos que contengan los datos \_ \_ garantizados. Los campos pueden ser campos de cadena o enteros.

Registro INSTALLMESSAGE \_ ACTIONDATA.



| Campo | Tipo   | Datos                    |
|-------|--------|-------------------------|
| 0     | string | null                    |
| 1     | int    | 2                       |
| 2     | string | ActionData para MyAction |



 

INSTALLMESSAGE \_ FILESINUSE

El registro FILESINUSE es un registro de longitud variable.



| Campo | Descripción                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Este campo puede ser NULL. Para una instalación con una interfaz de usuario básica, este campo puede especificar texto estático para mostrar en el [control ListBox](listbox-control.md) del [cuadro de diálogo FilesInUse](filesinuse-dialog.md). Para una instalación con una interfaz de usuario completa, este campo no tiene ningún efecto porque el texto se especifica mediante la creación del cuadro de diálogo FilesInUse personalizado. |
| 1     | Nombre del archivo en uso.                                                                                                                                                                                                                                                                                                                                        |
| 2     | Este campo identifica el proceso que contiene el archivo en uso. **Windows Installer versión 4.0:** El identificador de proceso (PID) del proceso o el título de la ventana del proceso.<br/> **Windows Installer versión 3.1 y anteriores:** Este campo debe ser el identificador de proceso (PID) del proceso.<br/>                                                      |



 

Por ejemplo, para enviar un mensaje FilesInUse que muestra dos archivos en uso, red.exe y blue.exe, el registro tiene cuatro campos más el campo 0. El formato del registro sería el que se muestra en la tabla siguiente. Este ejemplo requiere Windows Installer versión 4.0.

**Windows Installer versión 3.1 y anteriores:** Los campos 2 y 4 del ejemplo siguiente deben contener los PID de los procesos que contienen red.exe y blue.exe en uso.



| Campo | Descripción       |
|-------|-------------------|
| 0     | null              |
| 1     | Red.exe           |
| 2     | Título de la ventana roja  |
| 3     | Blue.exe          |
| 4     | Título de la ventana azul |



 

> [!Note]  
> En Windows Installer versión 4.0, si el PID pasado desde el servicio no tiene un título de ventana, como una aplicación de bandeja del sistema, el archivo no se muestra y el registro detallado contiene los mensajes siguientes.

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

INSTALLMESSAGE \_ RESOLVESOURCE

El registro INSTALLMESSAGE \_ RESOLVESOURCE tiene siete campos. Para que INSTALLMESSAGE RESOLVESOURCE funcione correctamente, es posible que un controlador de interfaz de usuario externo \_ no controle el mensaje INSTALLMESSAGE \_ RESOLVESOURCE. Windows El instalador debe controlar el mensaje INSTALLMESSAGE \_ RESOLVESOURCE. Es decir, el controlador de interfaz de usuario externo devuelve 0 para indicar que "no se ha realizado ninguna acción" al filtrar el mensaje INSTALLMESSAGE \_ RESOLVESOURCE. El procedimiento recomendado es evitar el envío de un mensaje RESOLVESOURCE.



| Campo | Descripción                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | null                                                                                                                                                               |
| 1     | null                                                                                                                                                               |
| 2     | Nombre del paquete.                                                                                                                                                      |
| 3     | Código de producto.                                                                                                                                                      |
| 4     | Ruta de acceso relativa si se conoce, puede ser NULL.                                                                                                                               |
| 5     | 0                                                                                                                                                                  |
| 6     | Si se va a validar el código del paquete. Un valor de "1" indica que se debe validar el código del paquete. Un valor de "0" indica que no se debe validar el paquete. |
| 7     | Disco necesario de la tabla multimedia. Un valor de "0" indica que cualquier disco es aceptable.                                                                              |



 

 

 




