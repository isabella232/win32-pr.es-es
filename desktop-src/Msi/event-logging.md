---
description: Windows Los eventos proporcionan una manera estándar y centralizada para que las aplicaciones (y el sistema operativo) registren eventos importantes de software y hardware.
ms.assetid: 1f28cbce-b759-4293-8af2-15f86f23228c
title: Registro de eventos (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7fdaf29ec0c638d3c85b82c74cca2bbede63c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158446"
---
# <a name="event-logging-windows-installer"></a>Registro de eventos (Windows instalador)

[Windows Events proporciona](../events/windows-events.md) una manera estándar y centralizada para que las aplicaciones (y el sistema operativo) registren eventos importantes de software y hardware. El servicio de registro de eventos almacena eventos de varios orígenes en una sola colección denominada registro *de eventos*. Antes de Windows Vista, usaría seguimiento de eventos [para Windows](../etw/event-tracing-portal.md) (ETW) o registro de eventos [para](../eventlog/event-logging.md) registrar eventos. Windows Vista introdujo un nuevo modelo de eventos que unifica ETW y Windows [Event Log](../wes/windows-event-log.md) API.

El instalador también escribe entradas en el registro de eventos. Estos eventos de registro son los siguientes:

-   Correcto o error de la instalación; eliminación o reparación de un producto.
-   Errores que se producen durante la configuración del producto.
-   Detección de datos de configuración dañados.

Si se escribe una gran cantidad de información, el archivo de registro de eventos puede estar lleno y el instalador muestra el mensaje "El archivo de registro de aplicación está lleno".

El instalador puede escribir las siguientes entradas en el registro de eventos. Todos los mensajes del registro de eventos tienen un identificador de evento único. Todos los errores generales que se han escrito en la tabla [Error](error-table.md) que se devuelven para una instalación que produce un error se registran en el registro de eventos de la aplicación con un identificador de mensaje igual al error + 10 000. Por ejemplo, el número de error de la tabla Error de una instalación completada correctamente es 1707. La instalación correcta se registra en el registro de eventos de la aplicación con un identificador de mensaje de 11707 (1707 + 10 000).

Para obtener información sobre cómo habilitar el registro detallado en el equipo de un usuario al solucionar problemas de implementación, vea Windows [procedimientos](windows-installer-best-practices.md)recomendados del instalador .



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
<td>Error de detección del producto '%1', característica '%2' durante la solicitud del componente '%3'</td>
<td>Mensaje de advertencia. Para obtener más información, <a href="searching-for-a-broken-feature-or-component.md">vea Buscar una característica o componente rotos.</a></td>
</tr>
<tr class="even">
<td>1002</td>
<td>Valor inesperado o ausente (nombre: '%1', valor: '%2') en la clave '%3'</td>
<td>Mensaje de error que indica que había un valor inesperado o que faltaba.</td>
</tr>
<tr class="odd">
<td>1003</td>
<td>Subclave inesperada o que falta '%1' en la clave '%2'</td>
<td>Mensaje de error que indica que había una subclave inesperada o que faltaba.</td>
</tr>
<tr class="even">
<td>1004</td>
<td>Detección del producto "%1", característica "%2", componente "%3" error <strong>Nota:</strong> A partir de la versión 2.0 del instalador de Windows, este mensaje es: Detección del producto '%1', característica '%2', error del componente '%3'. El recurso '%4' no existe.<br/></td>
<td>Mensaje de advertencia. Vea también <a href="searching-for-a-broken-feature-or-component.md">Buscar una característica o componente rotos.</a></td>
</tr>
<tr class="odd">
<td>1005</td>
<td>La operación de instalación inició un reinicio</td>
<td>Mensaje informativo que indica que la instalación inició un reinicio del sistema.</td>
</tr>
<tr class="even">
<td>1006</td>
<td>No se puede realizar la comprobación de la firma digital para el gabinete '%1'. WinVerifyTrust no está disponible en el equipo.</td>
<td>Mensaje de advertencia. Se hizo un archivador en la <a href="msidigitalsignature-table.md">tabla MsiDigitalSignature</a> para que se realizara una <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust"><strong>comprobación de WinVerifyTrust.</strong></a> Esta acción no se pudo realizar porque el equipo no tiene instalados los archivos DLL de criptografía adecuados.</td>
</tr>
<tr class="odd">
<td>1007</td>
<td>La directiva de restricción de software no permite la instalación de %1. El Windows solo permite la ejecución de elementos sin restricciones. El nivel de autorización devuelto por la directiva de restricción de software era %2.</td>
<td>Mensaje de error que indica que el administrador ha configurado la directiva de restricción de software para no permitir esta instalación.</td>
</tr>
<tr class="even">
<td>1008</td>
<td>No se permite la instalación de %1 debido a un error en el procesamiento de directivas de restricción de software. El objeto no puede ser de confianza.</td>
<td>Mensaje de error que indica que hubo problemas al intentar comprobar el paquete según la directiva de restricción de software.</td>
</tr>
<tr class="odd">
<td>1012</td>
<td>Esta versión de Windows no admite la implementación de paquetes de 64 bits. El script '%1' es para un paquete de 64 bits.</td>
<td>Mensaje de error que indica que los scripts de paquetes de 64 bits solo se pueden ejecutar en un equipo de 64 bits.</td>
</tr>
<tr class="even">
<td>1013</td>
<td>{Informe de excepciones no controladas}</td>
<td>Mensaje de error para una excepción no controlada, este es el informe.</td>
</tr>
<tr class="odd">
<td>1014</td>
<td>Windows Información del proxy del instalador no registrada correctamente</td>
<td>Mensaje de error que indica que la información del proxy no se registró correctamente.</td>
</tr>
<tr class="even">
<td>1015</td>
<td>No se pudo conectar al servidor. Error: %d</td>
<td>Mensaje informativo que indica que la instalación no se pudo conectar al servidor.</td>
</tr>
<tr class="odd">
<td>1016</td>
<td>Error de detección del producto "%1", característica "%2", componente "%3". No se pudo encontrar el recurso '%4' en un componente de ejecución desde el origen porque no se encontró ningún origen válido y accesible.</td>
<td>Mensaje de advertencia. Para obtener más información, <a href="searching-for-a-broken-feature-or-component.md">vea Buscar una característica o componente rotos.</a></td>
</tr>
<tr class="even">
<td>1017</td>
<td>El SID del usuario ha cambiado de "%1" a "%2", pero la aplicación administrada y las claves de datos de usuario no se pueden actualizar. Error = '%3'.</td>
<td>Mensaje de error que indica que se produjo un error al intentar actualizar el registro del usuario después de cambiar el SID del usuario.</td>
</tr>
<tr class="odd">
<td>1018</td>
<td>No se puede instalar la aplicación '%1' porque no es compatible con esta versión de Windows.</td>
<td>Mensaje de error que indica que la instalación no es compatible con la versión en ejecución de Windows. Póngase en contacto con el fabricante del software que se va a instalar para obtener una actualización.</td>
</tr>
<tr class="even">
<td>1019</td>
<td>Producto: %1: la actualización "%2" se quitó correctamente.</td>
<td>Mensaje informativo que indica que el instalador ha quitado la actualización. <strong>Windows Installer 2.0:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1020</td>
<td>Producto: %1: no se pudo quitar la actualización "%2". Código de error %3. Hay información adicional disponible en el archivo de registro %4.</td>
<td>Mensaje de error que indica que el instalador no pudo quitar la actualización. Hay información adicional disponible en el archivo de registro. <strong>Windows Installer 2.0:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1021</td>
<td>Producto: %1: no se pudo quitar la actualización "%2". Código de error %3.</td>
<td>Mensaje de error que indica que el instalador no pudo quitar la actualización. Para obtener información sobre cómo activar el registro, vea Habilitar el registro detallado en el equipo del usuario <a href="windows-installer-best-practices.md">al solucionar problemas de implementación.</a> <strong>Windows Installer 2.0:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1022</td>
<td>Producto: %1: actualización "%2" instalada correctamente.</td>
<td>Mensaje informativo que indica que el instalador ha instalado la actualización correctamente. <strong>Windows Installer 2.0:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1023</td>
<td>Producto: %1: no se pudo instalar la actualización "%2". Código de error %3. Hay información adicional disponible en el archivo de registro %4.</td>
<td>Mensaje de error que indica que el instalador no pudo instalar la actualización. Hay información adicional disponible en el archivo de registro. <strong>Windows Installer 2.0:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1024</td>
<td>Producto: %1: no se pudo instalar la actualización "%2". Código de error %3.</td>
<td>Mensaje de error que indica que el instalador no pudo instalar la actualización. Para obtener información sobre cómo activar el registro, vea Habilitar el registro detallado en el equipo del usuario <a href="windows-installer-best-practices.md">al solucionar problemas de implementación.</a> <strong>Windows Installer 2.0:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1025</td>
<td>Producto: %1. El siguiente proceso está utilizando el archivo %2: Nombre: %3 e Id. %4.</td>
<td><strong>Windows Installer 2.0:</strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1026</td>
<td>Windows El instalador ha determinado que su clave del Registro de datos de configuración no se ha protegido correctamente. El propietario de la clave debe ser Sistema local o Integrado\Administradores. La clave existente se eliminará y se volverá a crear con la configuración de seguridad adecuada.</td>
<td>Mensaje de advertencia. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1027</td>
<td>Windows El instalador ha determinado que una subclave del Registro %1 dentro de sus datos de configuración no se ha protegido correctamente. El propietario de la clave debe ser Sistema local o Integrado\Administradores. Se eliminará la subclave existente y todo su contenido.</td>
<td>Mensaje de advertencia. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1028</td>
<td>Windows El instalador ha determinado que su carpeta de caché de datos de configuración no se ha protegido correctamente. El propietario de la clave debe ser Sistema local o Integrado\Administradores. La carpeta existente se eliminará y se volverá a crear con la configuración de seguridad adecuada.</td>
<td>Mensaje de<strong><a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones</a>anteriores:</strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1029</td>
<td>Producto: %1. Se requiere reiniciar.</td>
<td>Mensaje de advertencia que indica que se requiere un reinicio del sistema para completar la instalación y que el reinicio se ha aplazado más adelante. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1030</td>
<td>Producto: %1. La aplicación intentó instalar una versión más reciente del archivo de Windows protegido %2. Es posible que tenga que actualizar el sistema operativo para que esta aplicación funcione correctamente. (Versión del paquete: %3, versión protegida del sistema operativo: %4).</td>
<td>Mensaje de advertencia que indica que la instalación intentó reemplazar un archivo crítico protegido por <a href="windows-resource-protection-on-windows-vista.md">Windows Resource Protection</a>. Es posible que se requiera una actualización del sistema operativo para usar esta aplicación. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>1031</td>
<td>Producto: %1. El ensamblado '%2' para el componente '%3' está en uso.</td>
<td>Mensaje de advertencia que indica que la instalación intentó actualizar un ensamblado actualmente en uso. El sistema debe reiniciarse para completar la actualización de este ensamblado. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/></td>
</tr>
<tr class="odd">
<td>1032</td>
<td>Error al actualizar las variables de entorno actualizadas durante la instalación de '%1'.</td>
<td>Mensaje de advertencia que indica que es posible que algunos usuarios que han iniciado sesión en el equipo deban cerrar sesión y volver a iniciarla para completar la actualización de las variables de entorno. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/></td>
</tr>
<tr class="even">
<td>3082</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Instalación completada con el estado: %4. Fabricante: %5.</td>
<td>Campo 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/> Campo 5: <a href="manufacturer.md"> <strong>Fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows instalador 4.5 y versiones anteriores:</a></strong> El campo 5 no está disponible.<br/></td>
</tr>
<tr class="odd">
<td>1034</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Eliminación completada con el estado: %4. Fabricante: %5.</td>
<td>Campo 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/> Campo 5: <a href="manufacturer.md"> <strong>Fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows instalador 4.5 y versiones anteriores:</a></strong> El campo 5 no está disponible.<br/></td>
</tr>
<tr class="even">
<td>1035</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Cambio de configuración completado con el estado: %4. Fabricante: %5.</td>
<td>Campo 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 5: <a href="manufacturer.md"> <strong>Fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows instalador 4.5 y versiones anteriores:</a></strong> El campo 5 no está disponible.<br/></td>
</tr>
<tr class="odd">
<td>1036</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Actualización: %4. Actualización de la instalación completada con el estado: %5. Fabricante: %6.</td>
<td>Campo 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 4: este es el nombre descriptivo si la tabla <a href="msipatchmetadata-table.md">MsiPatchMetadata</a> está presente en el paquete de revisión. De lo contrario, este es el GUID del código de revisión de la revisión.<br/> Campo 5: Estado de la instalación de la actualización.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/> Campo 6: <a href="manufacturer.md"> <strong>Fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows instalador 4.5 y versiones anteriores:</a></strong> El campo 6 no está disponible.<br/></td>
</tr>
<tr class="even">
<td>1037</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Actualización: %4. La eliminación de la actualización se completó con el estado: %5. Fabricante: %6.</td>
<td>Campo 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Campo 4: este es el nombre descriptivo si la tabla <a href="msipatchmetadata-table.md">MsiPatchMetadata</a> está presente en el paquete de revisión. De lo contrario, este es el GUID del código de revisión de la revisión.<br/> Campo 5: Estado de eliminación de actualizaciones.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/> Campo 6: <a href="manufacturer.md"> <strong>Fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 y versiones anteriores:</a></strong> El campo 6 no está disponible.<br/></td>
</tr>
<tr class="odd">
<td>1038</td>
<td>Producto: %1. Versión: %2. Idioma: %3. Se requiere reiniciar. Tipo de reinicio: %4. Motivo del reinicio: %5. Fabricante: %6.</td>
<td>Campo 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2 - <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Campo 3: <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <dl> Campo 4: constante que indica el tipo de reinicio: <br/> <dl> <strong>msirbRebootImmediate</strong> (1): se ha reiniciado inmediatamente el equipo.<br />
<strong>msirbRebootDeferred</strong> (2): un usuario o administrador ha aplazado un reinicio necesario del equipo mediante la interfaz de usuario o <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress.<br />
</dl> </dd> Field 5 - A constant indicating the reason for the restart:<br/> <dl> <strong>msirbRebootUndeterminedReason</strong> (0): se requiere reiniciar por un motivo no especificado.<br />
<strong>msirbRebootInUseFilesReason</strong> (1): se requiere un reinicio para reemplazar los archivos en uso.<br />
<strong>msirbRebootScheduleRebootReason</strong> (2): el paquete contiene una <a href="schedulereboot-action.md">acción ScheduleReboot.</a><br />
<strong>msirbRebootForceRebootReason</strong> (3): el paquete contiene una <a href="forcereboot-action.md">acción ForceReboot.</a><br />
<strong>msirbRebootCustomActionReason</strong> (4): una acción personalizada denominada función <a href="/windows/desktop/api/Msiquery/nf-msiquery-msisetmode"><strong>MsiSetMode.</strong></a><br />
</dl> </dd> </dl> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 y versiones anteriores:</a></strong> No disponible.<br/> Campo 6: <a href="manufacturer.md"> <strong>Fabricante</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 y versiones anteriores:</a></strong> El campo 6 no está disponible.<br/></td>
</tr>
<tr class="even">
<td>10005</td>
<td>El instalador ha detectado un error inesperado al instalar este paquete. Esto puede deberse a un problema del paquete. El código de error es [1]. {{Los argumentos son: [2], [3], [4]}}</td>
<td>Mensaje de error que indica que se ha producido un error interno. El texto de este mensaje se basa en el texto que se ha escrito para el error 5 en la tabla Error.</td>
</tr>
<tr class="odd">
<td>11707</td>
<td>Producto [2]: la operación de instalación se completó correctamente</td>
<td>Mensaje informativo que indica que la instalación del producto se ha realizado correctamente.</td>
</tr>
<tr class="even">
<td>11708</td>
<td>Producto [2]: error en la operación de instalación</td>
<td>Mensaje de error que indica que se produjo un error en la instalación del producto.</td>
</tr>
<tr class="odd">
<td>11728</td>
<td>Producto [2]: la configuración se completó correctamente.</td>
<td>Mensaje informativo que indica que la configuración del producto se ha realizado correctamente.</td>
</tr>
</tbody>
</table>



 

Puede importar cadenas de errores localizados para eventos en la base de datos mediante Msidb.exe [**o MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). El SDK incluye cadenas de recursos localizadas para cada uno de los idiomas enumerados en la sección Localización de las tablas [Error y ActionText.](localizing-the-error-and-actiontext-tables.md) Si no se rellenan las cadenas de error correspondientes a eventos, el instalador carga cadenas localizadas para el idioma especificado por la [**propiedad ProductLanguage.**](productlanguage.md)

 

 
