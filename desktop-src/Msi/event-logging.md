---
description: Los eventos de Windows proporcionan una manera centralizada y estándar para que las aplicaciones (y el sistema operativo) registren eventos importantes de software y hardware.
ms.assetid: 1f28cbce-b759-4293-8af2-15f86f23228c
title: Registro de eventos (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7fdaf29ec0c638d3c85b82c74cca2bbede63c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812872"
---
# <a name="event-logging-windows-installer"></a>Registro de eventos (Windows Installer)

[Los eventos de Windows](../events/windows-events.md) proporcionan una manera centralizada y estándar para que las aplicaciones (y el sistema operativo) registren eventos importantes de software y hardware. El servicio de registro de eventos almacena eventos de varios orígenes en una sola colección denominada *registro de eventos*. Antes de Windows Vista, usaría el [seguimiento de eventos para Windows](../etw/event-tracing-portal.md) (ETW) o el [registro de eventos](../eventlog/event-logging.md) para registrar los eventos. Windows Vista presentó un nuevo modelo de eventos que unifica ETW y la API del [registro de eventos de Windows](../wes/windows-event-log.md) .

El instalador también escribe entradas en el registro de eventos. Estos eventos de registro, como los siguientes:

-   Éxito o error de la instalación; eliminación o reparación de un producto.
-   Errores que se producen durante la configuración del producto.
-   Detección de datos de configuración dañados.

Si se escribe una gran cantidad de información, el archivo de registro de eventos puede llenarse y el instalador muestra el mensaje "el archivo de registro de la aplicación está lleno".

El instalador puede escribir las siguientes entradas en el registro de eventos. Todos los mensajes del registro de eventos tienen un identificador de evento único. Todos los errores generales creados en la [tabla de errores](error-table.md) que se devuelven para una instalación con errores se registran en el registro de eventos de aplicación con un ID. de mensaje igual al Error + 10.000. Por ejemplo, el número de error de la tabla de errores de una instalación se completó correctamente es 1707. La instalación correcta se registra en el registro de eventos de aplicación con un ID. de mensaje de 11707 (1707 + 10.000).

Para obtener información acerca de cómo habilitar el registro detallado en el equipo de un usuario al solucionar problemas de implementación, consulte [Windows Installer prácticas recomendadas](windows-installer-best-practices.md).



<table>
<thead>
<tr class="header">
<th>Id. de evento</th>
<th>Message</th>
<th>Observaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1001</td>
<td>No se pudo detectar el producto ' %1 ', característica ' %2 ' durante la solicitud del componente ' %3 '</td>
<td>Un mensaje de advertencia. Para obtener más información, vea <a href="searching-for-a-broken-feature-or-component.md">buscar una característica o componente interrumpido</a>.</td>
</tr>
<tr class="even">
<td>1002</td>
<td>Falta un valor o es inesperado (nombre: ' %1 ', valor: ' %2 ') en la clave ' %3 '</td>
<td>Mensaje de error que indica que hubo un valor inesperado o falta.</td>
</tr>
<tr class="odd">
<td>1003</td>
<td>Falta la subclave ' %1 ' inesperada o no se encuentra en la clave ' %2 '</td>
<td>Mensaje de error que indica que había una subclave inesperada o falta.</td>
</tr>
<tr class="even">
<td>1004</td>
<td>No se pudo detectar el producto ' %1 ', característica ' %2 ', componente ' %3 ' <strong>Nota:</strong> a partir de Windows Installer versión 2,0, este mensaje es: no se pudo detectar el producto ' %1 ', característica ' %2 ', componente ' %3 '. El recurso ' %4 ' no existe.<br/></td>
<td>Un mensaje de advertencia. Vea también <a href="searching-for-a-broken-feature-or-component.md">buscar una característica o componente interrumpido</a>.</td>
</tr>
<tr class="odd">
<td>1005</td>
<td>La operación de instalación inició un reinicio</td>
<td>Mensaje informativo de que la instalación ha iniciado el reinicio del sistema.</td>
</tr>
<tr class="even">
<td>1006</td>
<td>No se puede realizar la comprobación de la firma digital para el archivo. cab ' %1 '. WinVerifyTrust no está disponible en el equipo.</td>
<td>Mensaje de advertencia. Se creó un archivo. cab en la <a href="msidigitalsignature-table.md">tabla MsiDigitalSignature</a> para tener una comprobación <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust"><strong>WinVerifyTrust</strong></a> realizada. Esta acción no se pudo realizar porque el equipo no tiene instaladas las DLL criptográficas adecuadas.</td>
</tr>
<tr class="odd">
<td>1007</td>
<td>La Directiva de restricción de software no permite la instalación de %1. El Windows Installer solo permite la ejecución de elementos sin restricciones. El nivel de autorización devuelto por la Directiva de restricción de software era %2.</td>
<td>Un mensaje de error que indica que el administrador ha configurado la Directiva de restricción de software para no permitir esta instalación.</td>
</tr>
<tr class="even">
<td>1008</td>
<td>No se permite la instalación de %1 debido a un error en el procesamiento de la Directiva de restricción de software. No se puede confiar en el objeto.</td>
<td>Un mensaje de error que indica que hubo problemas al intentar comprobar el paquete de acuerdo con la Directiva de restricción de software.</td>
</tr>
<tr class="odd">
<td>1012</td>
<td>Esta versión de Windows no admite la implementación de paquetes de 64 bits. El script ' %1 ' es para un paquete de 64 bits.</td>
<td>Mensaje de error que indica que los scripts de los paquetes de 64 bits solo se pueden ejecutar en un equipo de 64 bits.</td>
</tr>
<tr class="even">
<td>1013</td>
<td>{Informe de excepción no controlada}</td>
<td>Mensaje de error para una excepción no controlada, este es el informe.</td>
</tr>
<tr class="odd">
<td>1014</td>
<td>Windows Installer la información de proxy no está registrada correctamente</td>
<td>Mensaje de error que indica que la información de proxy no se registró correctamente.</td>
</tr>
<tr class="even">
<td>1015</td>
<td>No se pudo conectar al servidor. Error:% d</td>
<td>Mensaje informativo de que la instalación no se pudo conectar al servidor.</td>
</tr>
<tr class="odd">
<td>1016</td>
<td>No se pudo detectar el producto ' %1 ', característica ' %2 ', componente ' %3 '. No se pudo encontrar el recurso ' %4 ' en un componente de origen de ejecución porque no se encontró ningún origen válido y accesible.</td>
<td>Mensaje de advertencia. Para obtener más información, vea <a href="searching-for-a-broken-feature-or-component.md">buscar una característica o componente interrumpido</a>.</td>
</tr>
<tr class="even">
<td>1017</td>
<td>El SID de usuario ha cambiado de ' %1 ' a ' %2 ', pero no se puede actualizar la aplicación administrada ni las claves de datos del usuario. Error = ' %3 '.</td>
<td>Mensaje de error que indica que se ha producido un error al intentar actualizar el registro del usuario después de cambiar el SID del usuario.</td>
</tr>
<tr class="odd">
<td>1018</td>
<td>No se puede instalar la aplicación ' %1 ' porque no es compatible con esta versión de Windows.</td>
<td>Mensaje de error que indica que la instalación de no es compatible con la versión de Windows que se está ejecutando actualmente. Póngase en contacto con el fabricante del software que se va a instalar para obtener una actualización.</td>
</tr>
<tr class="even">
<td>1019</td>
<td>Producto: %1-se quitó correctamente la actualización ' %2 '.</td>
<td>Mensaje informativo de que el instalador ha quitado la actualización. <strong>Windows Installer 2,0:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1020</td>
<td>Producto: %1-no se pudo quitar la actualización ' %2 '. Código de error %3. Hay información adicional disponible en el archivo de registro %4.</td>
<td>Mensaje de error que indica que el instalador no pudo quitar la actualización. Hay información adicional disponible en el archivo de registro. <strong>Windows Installer 2,0:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1021</td>
<td>Producto: %1-no se pudo quitar la actualización ' %2 '. Código de error %3.</td>
<td>Mensaje de error que indica que el instalador no pudo quitar la actualización. Para obtener información sobre cómo activar el registro, consulte <a href="windows-installer-best-practices.md">Habilitar el registro detallado en el equipo del usuario al solucionar problemas de implementación.</a> <strong>Windows Installer 2,0:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1022</td>
<td>Producto: %1-actualización ' %2 ' instalada correctamente.</td>
<td>Mensaje informativo de que el instalador ha instalado la actualización correctamente. <strong>Windows Installer 2,0:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1023</td>
<td>Producto: %1-no se pudo instalar la actualización ' %2 '. Código de error %3. Hay información adicional disponible en el archivo de registro %4.</td>
<td>Mensaje de error que indica que el instalador no pudo instalar la actualización. Hay información adicional disponible en el archivo de registro. <strong>Windows Installer 2,0:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1024</td>
<td>Producto: %1-no se pudo instalar la actualización ' %2 '. Código de error %3.</td>
<td>Mensaje de error que indica que el instalador no pudo instalar la actualización. Para obtener información sobre cómo activar el registro, consulte <a href="windows-installer-best-practices.md">Habilitar el registro detallado en el equipo del usuario al solucionar problemas de implementación.</a> <strong>Windows Installer 2,0:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1025</td>
<td>Producto: %1. El archivo %2 se está usando en el siguiente proceso: nombre: %3, ID. %4.</td>
<td><strong>Windows Installer 2,0:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1026</td>
<td>Windows Installer ha determinado que la clave del registro de datos de configuración no se protegió correctamente. El propietario de la clave debe ser sistema local o Builtin\Administrators. La clave existente se eliminará y se volverá a crear con la configuración de seguridad adecuada.</td>
<td>Mensaje de advertencia. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1027</td>
<td>Windows Installer ha determinado que una subclave del registro %1 dentro de sus datos de configuración no se protegió correctamente. El propietario de la clave debe ser sistema local o Builtin\Administrators. La subclave existente y todo su contenido se eliminarán.</td>
<td>Mensaje de advertencia. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1028</td>
<td>Windows Installer ha determinado que la carpeta de caché de datos de configuración no se protegió correctamente. El propietario de la clave debe ser sistema local o Builtin\Administrators. La carpeta existente se eliminará y se volverá a crear con la configuración de seguridad adecuada.</td>
<td>Mensaje<strong><a href="not-supported-in-windows-installer-version-3-1.md">de advertencia Windows Installer 3,1 y versiones anteriores</a>:</strong> no disponible.<br/></td>
</tr>
<tr class="even">
<td>1029</td>
<td>Producto: %1. Es necesario reiniciar.</td>
<td>Mensaje de advertencia indicatiing que es necesario reiniciar el sistema para completar la instalación y que el reinicio se ha aplazado a una hora posterior. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1030</td>
<td>Producto: %1. La aplicación intentó instalar una versión más reciente del archivo de Windows protegido %2. Es posible que tenga que actualizar el sistema operativo para que esta aplicación funcione correctamente. (Versión del paquete: %3, versión protegida del sistema operativo: %4).</td>
<td>Mensaje de advertencia que indica que la instalación intentó reemplazar un archivo crítico protegido por <a href="windows-resource-protection-on-windows-vista.md">protección de recursos de Windows</a>. Es posible que sea necesario actualizar el sistema operativo para usar esta aplicación. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1031</td>
<td>Producto: %1. El ensamblado ' %2 ' del componente ' %3 ' está en uso.</td>
<td>Mensaje de advertencia que indica que la instalación ha intentado actualizar un ensamblado actualmente en uso. El sistema debe reiniciarse para completar la actualización de este ensamblado. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1032</td>
<td>Error al actualizar las variables de entorno que se actualizaron durante la instalación de ' %1 '.</td>
<td>Mensaje de advertencia que indica que algunos usuarios que han iniciado sesión en el equipo pueden necesitar cerrar la sesión y volver a iniciarla para completar la actualización de las variables de entorno. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>3082</td>
<td>Producto: %1. Versión: %2. Idioma: %3. La instalación se completó con el estado: %4. Fabricante: %5.</td>
<td>Campo 1- <a href="productname.md"><strong>NombreProducto</strong></a> campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/> Campo 5: <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 y versiones anteriores</a>:</strong> Campo 5 no disponible.<br/></td>
</tr>
<tr class="odd">
<td>1034</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Eliminación completada con estado: %4. Fabricante: %5.</td>
<td>Campo 1- <a href="productname.md"><strong>NombreProducto</strong></a> campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/> Campo 5: <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 y versiones anteriores</a>:</strong> Campo 5 no disponible.<br/></td>
</tr>
<tr class="even">
<td>1035</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Cambio de configuración completado con estado: %4. Fabricante: %5.</td>
<td>Campo 1- <a href="productname.md"><strong>NombreProducto</strong></a> campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 5: <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 y versiones anteriores</a>:</strong> Campo 5 no disponible.<br/></td>
</tr>
<tr class="odd">
<td>1036</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Actualización: %4. La instalación de la actualización se completó con el estado: %5. Fabricante: %6.</td>
<td>Campo 1- <a href="productname.md"><strong>NombreProducto</strong></a> campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 4: es el nombre descriptivo de usuario si la <a href="msipatchmetadata-table.md">tabla MsiPatchMetadata</a> está presente en el paquete de revisión. De lo contrario, es el GUID del código de revisión de la revisión.<br/> Campo 5: estado de la instalación de la actualización.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/> Campo 6: <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 y versiones anteriores</a>:</strong> El campo 6 no está disponible.<br/></td>
</tr>
<tr class="even">
<td>1037</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Actualización: %4. Eliminación de la actualización completada con el estado: %5. Fabricante: %6.</td>
<td>Campo 1- <a href="productname.md"><strong>NombreProducto</strong></a> campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 4: es el nombre descriptivo de usuario si la <a href="msipatchmetadata-table.md">tabla MsiPatchMetadata</a> está presente en el paquete de revisión. De lo contrario, es el GUID del código de revisión de la revisión.<br/> Campo 5: estado de eliminación de la actualización.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/> Campo 6: <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 y versiones anteriores</a>:</strong> El campo 6 no está disponible.<br/></td>
</tr>
<tr class="odd">
<td>1038</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Se requiere reiniciar. Tipo de reinicio: %4. Motivo de reinicio: %5. Fabricante: %6.</td>
<td>Campo 1- <a href="productname.md"><strong>NombreProducto</strong></a> campo 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <dl> Campo 4: constante que indica el tipo de reinicio: <br/> <dl> <strong>msirbRebootImmediate</strong> (1): se produjo un reinicio inmediato del equipo.<br />
<strong>msirbRebootDeferred</strong> (2): un usuario o administrador ha diferido un reinicio necesario del equipo mediante la interfaz de usuario o <a href="reboot.md"><strong>reinicio</strong></a>= ReallySuppress.<br />
</dl> </dd> Field 5 - A constant indicating the reason for the restart:<br/> <dl> <strong>msirbRebootUndeterminedReason</strong> (0): se requiere un reinicio por un motivo no especificado.<br />
<strong>msirbRebootInUseFilesReason</strong> (1): se requiere un reinicio para reemplazar los archivos que se están usando.<br />
<strong>msirbRebootScheduleRebootReason</strong> (2): el paquete contiene una acción <a href="schedulereboot-action.md">ScheduleReboot</a> .<br />
<strong>msirbRebootForceRebootReason</strong> (3): el paquete contiene una acción <a href="forcereboot-action.md">ForceReboot</a> .<br />
<strong>msirbRebootCustomActionReason</strong> (4): una acción personalizada llamada a la función <a href="/windows/desktop/api/Msiquery/nf-msiquery-msisetmode"><strong>MsiSetMode</strong></a> .<br />
</dl> </dd> </dl> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 y versiones anteriores</a>:</strong> No disponible.<br/> Campo 6: <a href="manufacturer.md"> <strong>fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 y versiones anteriores</a>:</strong> El campo 6 no está disponible.<br/></td>
</tr>
<tr class="even">
<td>10005</td>
<td>El instalador ha encontrado un error inesperado al instalar este paquete. Esto puede deberse a un problema del paquete. El código de error es [1]. {{Los argumentos son: [2], [3], [4]}}</td>
<td>Mensaje de error que indica que se ha producido un error interno. El texto de este mensaje se basa en el texto creado para el error 5 en la tabla de errores.</td>
</tr>
<tr class="odd">
<td>11707</td>
<td>Producto [2]: operación de instalación completada correctamente</td>
<td>Mensaje informativo de que la instalación del producto se ha realizado correctamente.</td>
</tr>
<tr class="even">
<td>11708</td>
<td>Producto [2]: error en la operación de instalación</td>
<td>Mensaje de error que indica que se ha producido un error en la instalación del producto.</td>
</tr>
<tr class="odd">
<td>11728</td>
<td>Producto [2]: la configuración se completó correctamente.</td>
<td>Mensaje informativo de que la configuración del producto se realizó correctamente.</td>
</tr>
</tbody>
</table>



 

Puede importar cadenas de errores localizadas para eventos en la base de datos mediante Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). El SDK incluye cadenas de recursos localizadas para cada uno de los idiomas que aparecen en la sección [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md) . Si no se rellenan las cadenas de error correspondientes a los eventos, el instalador carga las cadenas localizadas para el idioma especificado por la propiedad [**ProductLanguage**](productlanguage.md) .

 

 
