---
description: Los mensajes enviados mediante MsiProcessMessage son los mismos que los recibidos por la función de \_ devolución de llamada del controlador INSTALLUI si se llamó a MsiSetExternalUI.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Envío de mensajes a Windows Installer mediante MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003039"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a>Envío de mensajes a Windows Installer mediante MsiProcessMessage

Los mensajes enviados mediante [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) son los mismos que los recibidos por la función de devolución de llamada del [**\_ controlador INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera) si se llamó a [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) . De lo contrario, Windows Installer controla los mensajes. Para obtener más información, consulte [análisis de mensajes de Windows Installer](parsing-windows-installer-messages.md).

Por ejemplo, para enviar un \_ mensaje de error INSTALLMESSAGE con el \_ icono MB ICONWARNING y los \_ botones ABORTRETRYCANCEL MB:


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



Donde *hInstall* es el identificador de la instalación, proporcionado a una acción personalizada o al identificador *hProduct* de [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) o [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), y *hRec* es el registro que contiene la información de error que se va a formatear. Para obtener información sobre cómo se realiza el formato, vea [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).

De forma predeterminada, si \_ se envía un mensaje de error INSTALLMESSAGE o INSTALLMESSAGE \_ FATALEXIT sin especificar tipos de botón o de icono, \_ se usan MB OK, no Icon y MB \_ DEFBUTTON1.

Windows Installer no etiqueta el botón **anular** con la cadena "Abort" al mostrar un cuadro de mensajes con la \_ especificación del botón MB ABORTRETRYIGNORE, en su lugar, etiqueta el botón con la cadena "Cancel". Todos los mensajes de error abstenerse de usar la palabra "Abort" y, en su lugar, usan la palabra "Cancel".

El parámetro *hRecord* de la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) depende del tipo de mensaje enviado al [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). En la siguiente lista se detallan los requisitos del registro en relación con el tipo de mensaje:

INSTALLMESSAGE \_ FATALEXIT

 

información de INSTALLMESSAGE \_

 

INSTALLMESSAGE \_ OUTOFDISKSPACE



| Campo         | Descripción                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Plantilla para el formato de la cadena resultante. Vea [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) para obtener más información. Se hace referencia a los campos del registro usando \[ 1 \] en el campo 1, \[ 2 \] para el campo 2, etc. |
| de 1 a *n* | Todos los campos siguientes están directamente relacionados con los campos a los que hace referencia la plantilla en el campo 0.                                                                                                                    |



 

Si el campo 0 es null, la cadena recibida por el controlador de la interfaz de usuario tiene el formato: 1: \[ datos del campo 1 \] 2: los \[ datos del campo 2 \] significa que para cada campo del registro, la cadena contiene el número de campo seguido de los datos almacenados en el campo.

Los mensajes de información de [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) se registran cuando [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), la [opción de línea de comandos](command-line-options.md)'/l ' o la [Directiva de registro](logging.md) especifican ' I ' o INSTALLLOGMODE \_ info.

\_error INSTALLMESSAGE

 

ADVERTENCIA de INSTALLMESSAGE \_

 

\_usuario INSTALLMESSAGE

Para utilizar un mensaje de la tabla de errores.



| Campo         | Descripción                                           |
|---------------|-------------------------------------------------------|
| 0             | Debe ser null.                                         |
| 1             | Número de mensaje en la [tabla de errores](error-table.md). |
| de 2 a *n* | Relacionado con el mensaje especificado en la tabla de errores.  |



 

Por ejemplo.



| Campo | Tipo   | Datos       |
|-------|--------|------------|
| 0     | string | null       |
| 1     | int    | 1304       |
| 2     | string | Myfile.txt |



 

El mensaje resultante recibido del controlador de la interfaz de usuario es:

Error 1304. Error al escribir en el archivo: Myfile.txt. Compruebe que tiene acceso a ese directorio.

Si el campo 0 no es null, se invalida el mensaje de la tabla de errores. En su lugar, la plantilla de campo 0 determina el formato del mensaje.

El mensaje también puede especificar los botones, incluido el botón predeterminado, y el icono para usarlo con el mensaje, como se mencionó anteriormente. Los tipos de icono y botón se enumeran en el [**\_ controlador INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera).

INSTALLMESSAGE \_ COMMONDATA

Este mensaje se envía para habilitar o deshabilitar el botón **Cancelar** en un cuadro de diálogo de progreso.



| Campo | Descripción                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Sin usar.                                                                                                                                      |
| 1     | 2 hace referencia al botón **Cancelar** .                                                                                                           |
| 2     | Un valor de 1 indica que el botón **Cancelar** debe estar visible. Un valor de 0 indica que el botón **Cancelar** debe ser invisible.<br/> |



 

Por ejemplo, para deshabilitar u ocultar el botón **Cancelar** , el registro tendría el siguiente aspecto.



| Campo | Tipo   | Datos |
|-------|--------|------|
| 0     | string | null |
| 1     | int    | 2    |
| 2     | int    | 0    |



 

INSTALLMESSAGE \_ ACTIONSTART

 

INSTALLMESSAGE \_ ACTIONDATA

El \_ registro ACTIONSTART de INSTALLMESSAGE determina el formato del registro ActionData.



| Campo | Descripción                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| 0     | null                                                                                                          |
| 1     | Nombre de la acción. El nombre de este campo no debe ser null.                                                         |
| 2     | Descripción de la acción.                                                                                           |
| 3     | Plantilla de acción. Se usa para el ActionData cuyo mensaje se está formateando según esta plantilla. |



 

No haga referencia al campo 0 en el mensaje de la plantilla de acción.

El registro de INSTALLMESSAGE \_ ACTIONDATA tiene el formato siguiente.



| Campo         | Descripción                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | null                                                                                                                                               |
| de 1 a *n* | Depende del campo 3 del \_ mensaje ACTIONSTART INSTALLMESSAGE correspondiente o de la plantilla especificada en la [tabla ActionText](actiontext-table.md). |



 

Por ejemplo, el \_ registro INSTALLMESSAGE ACTIONSTART.



| Campo | Tipo   | Datos                                                            |
|-------|--------|-----------------------------------------------------------------|
| 0     | string | null                                                            |
| 1     | string | OnAction                                                        |
| 2     | string | Esta es la descripción de "OnAction"                           |
| 3     | string | Plantilla OnAction: los datos de Campo1 son \[ 1 \] . los datos del campo 2 son \[ 2 \] . |



 

La plantilla para INSTALLMESSAGE \_ ACTIONSTART (campo 3) hace referencia a los campos 1 y 2, el \_ registro INSTALLMESSAGE ACTIONDATA debe tener 2 campos que contengan los datos garantizados. Los campos pueden ser campos de cadena o de entero.

INSTALLMESSAGE \_ ACTIONDATA.



| Campo | Tipo   | Datos                    |
|-------|--------|-------------------------|
| 0     | string | null                    |
| 1     | int    | 2                       |
| 2     | string | ActionData para OnAction |



 

INSTALLMESSAGE \_ FILESINUSE

El registro FILESINUSE es un registro de longitud variable.



| Campo | Descripción                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Este campo puede ser null. En el caso de una instalación con una interfaz de usuario básica, este campo puede especificar texto estático para su presentación en el [control ListBox](listbox-control.md) del [cuadro de diálogo FilesInUse](filesinuse-dialog.md). En el caso de una instalación con una interfaz de usuario completa, este campo no tiene ningún efecto porque el texto se especifica mediante la creación del cuadro de diálogo FilesInUse personalizado. |
| 1     | Nombre del archivo en uso.                                                                                                                                                                                                                                                                                                                                        |
| 2     | Este campo identifica el proceso que contiene el archivo en uso. **Windows Installer versión 4,0:** El identificador de proceso (PID) del proceso o el título de la ventana para el proceso.<br/> **Windows Installer versión 3,1 y versiones anteriores:** Este campo debe ser el ID. de proceso (PID) del proceso.<br/>                                                      |



 

Por ejemplo, para enviar un mensaje FilesInUse que muestre dos archivos en uso, red.exe y blue.exe, el registro tiene cuatro campos más el campo 0. El formato del registro sería como se muestra en la tabla siguiente. Este ejemplo requiere Windows Installer versión 4,0.

**Windows Installer versión 3,1 y versiones anteriores:** Los campos 2 y 4 del siguiente ejemplo deben contener los PID de los procesos que contienen red.exe y blue.exe en uso.



| Campo | Descripción       |
|-------|-------------------|
| 0     | null              |
| 1     | Red.exe           |
| 2     | Título de la ventana roja  |
| 3     | Blue.exe          |
| 4     | Título de la ventana azul |



 

> [!Note]  
> En Windows Installer versión 4,0, si el PID pasado desde el servicio no tiene un título de ventana, como una aplicación de bandeja del sistema, el archivo no se mostrará y el registro detallado contendrá los mensajes siguientes.

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

INSTALLMESSAGE \_ RESOLVESOURCE

El registro de INSTALLMESSAGE \_ RESOLVESOURCE tiene siete campos. Para \_ que INSTALLMESSAGE RESOLVESOURCE funcione correctamente, es posible que un controlador de interfaz de usuario externo no controle el \_ mensaje INSTALLMESSAGE RESOLVESOURCE. Windows Installer debe controlar el \_ mensaje RESOLVESOURCE de INSTALLMESSAGE. Es decir, el controlador de la interfaz de usuario externa devuelve 0 para indicar que no se ha realizado ninguna acción al filtrar el \_ mensaje RESOLVESOURCE de INSTALLMESSAGE. El procedimiento recomendado es evitar el envío de un mensaje RESOLVESOURCE.



| Campo | Descripción                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | null                                                                                                                                                               |
| 1     | null                                                                                                                                                               |
| 2     | Nombre del paquete.                                                                                                                                                      |
| 3     | Código de producto.                                                                                                                                                      |
| 4     | Ruta de acceso relativa, si se conoce, puede ser null.                                                                                                                               |
| 5     | 0                                                                                                                                                                  |
| 6     | Indica si se debe validar el código de paquete. Un valor de ' 1 ' indica que se debe validar el código de paquete. Un valor de "0" indica que el paquete no se debe validar. |
| 7     | Disco requerido de la tabla de medios. Un valor de "0" indica que cualquier disco es aceptable.                                                                              |



 

 

 




