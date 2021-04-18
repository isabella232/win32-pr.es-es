---
Descripción: el programa ejecutable que interpreta paquetes e instala productos es Msiexec.exe. Nota: msiexec también establece un nivel de error en la devolución que corresponde a los códigos de error del sistema. En la tabla siguiente se identifican las opciones de línea de comandos estándar para este programa. Las opciones de línea de comandos no distinguen mayúsculas de minúsculas. Windows Installer 2,0: las opciones de línea de comandos que se identifican en este tema están disponibles a partir de Windows Installer 3,0. Las opciones de Command-Line de Windows Installer están disponibles con Windows Installer&\# 160; 3.0 y versiones anteriores.
MS. AssetID: b1707c88-1cca-45ab-bb23-6002bfd5204e title: instalador estándar Command-Line opciones ms. topic: artículo ms. Date: 05/31/2018
---

# <a name="standard-installer-command-line-options"></a>Opciones de Command-Line del instalador estándar

El programa ejecutable que interpreta paquetes e instala productos es Msiexec.exe.

> [!Note]  
> Msiexec también establece un nivel de error en la devolución que corresponde a los [códigos de error del sistema](../debug/system-error-codes.md).

 

En la tabla siguiente se identifican las opciones de línea de comandos estándar para este programa. Las opciones de línea de comandos no distinguen mayúsculas de minúsculas.

**Windows Installer 2,0:** Las opciones de línea de comandos que se identifican en este tema están disponibles a partir de Windows Installer 3,0. Las [Opciones de línea de comandos](command-line-options.md) de Windows Installer están disponibles con Windows Installer 3,0 y versiones anteriores.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Opción</th>
<th>Parámetros</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/help</strong></td>
<td> </td>
<td>Opción de ayuda y referencia rápida. Muestra el uso correcto del comando de instalación, incluida una lista de todos los modificadores y el comportamiento. La descripción del uso se puede mostrar en la interfaz de usuario. El uso incorrecto de cualquier opción invoca esta opción de ayuda.<br/> Ejemplo: <strong>msiexec/Help</strong><br/>
<blockquote>
[!Note]<br />
La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Opción de pantalla silenciosa. El instalador ejecuta una instalación sin mostrar una interfaz de usuario. No se muestra al usuario ningún mensaje, mensaje o cuadro de diálogo. El usuario no puede cancelar la instalación. Use las opciones de línea de comandos <strong>/norestart</strong> o <strong>/forcerestart</strong> estándar para controlar los reinicios. Si no se especifica ninguna opción de reinicio, el programa de instalación reinicia el equipo siempre que sea necesario sin mostrar ningún mensaje o advertencia al usuario.<br/> Ejemplos: <br/> <strong>msiexec/Package Application.msi/Quiet</strong><br/> <strong>Msiexec/Uninstall Application.msi/Quiet</strong><br/> <strong>Msiexec/update msipatch. MSP/Quiet</strong><br/> <strong>Msiexec/Uninstall msipatch. MSP/Package Application.msi/Quiet</strong><br/>
<blockquote>
[!Note]<br />
La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/QN</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>Opción de presentación pasiva. El instalador muestra una barra de progreso al usuario que indica que hay una instalación en curso, pero no se muestra ningún mensaje de error ni mensajes de error al usuario. El usuario no puede cancelar la instalación. Use las opciones de línea de comandos <strong>/norestart</strong> o <strong>/forcerestart</strong> estándar para controlar los reinicios. Si no se especifica ninguna opción de reinicio, el programa de instalación reinicia el equipo siempre que sea necesario sin mostrar ningún mensaje o advertencia al usuario. <br/> Ejemplo: <strong>msiexec/package Application.msi/Passive</strong> <br/>
<blockquote>
[!Note]<br />
La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S establecida en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Opción de reinicio nunca. El instalador nunca reinicia el equipo después de la instalación.<br/> Ejemplo: msiexec/Package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
La línea de comandos de Windows Installer equivalente tiene el <a href="reboot.md"><strong>reinicio</strong></a>= ReallySuppress establecido en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>Opción de reinicio siempre. El instalador reinicia siempre el equipo después de cada instalación.<br/> Ejemplo: msiexec/Package Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
La línea de comandos de Windows Installer equivalente tiene el <a href="reboot.md"><strong>reinicio</strong></a>= Force establecido en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Preguntar antes de reiniciar. Muestra un mensaje que indica que es necesario reiniciar para completar la instalación y pregunta al usuario si desea reiniciar el sistema ahora. Esta opción no se puede usar junto con la opción <strong>/Quiet</strong> .<br/>
<blockquote>
[!Note]<br />
La línea de comandos de Windows Installer equivalente tiene <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; establecido en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/uninstall</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Opción de desinstalación del producto. Desinstala un producto.<br/>
<blockquote>
[!Note]<br />
La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/x</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/uninstall</strong></td>
<td><em>/Package <Package.msi | ProductCode> /Uninstall <Update1.msp | PatchGUID1> [; Update2. MSP | PatchGUID2]</em></td>
<td>Desinstalar opción de actualización. Desinstala una revisión de actualización.<br/>
<blockquote>
[!Note]<br />
La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/i</strong> con <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= update1. MSP | PatchGUID1[; Update2. MSP | PatchGUID2] establecido en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Opción de registro. Escribe información de registro en un archivo de registro en la ruta de acceso existente especificada. La ruta de acceso a la ubicación del archivo de registro ya debe existir. El instalador no crea la estructura de directorios para el archivo de registro.<br/> La siguiente información se especifica en el registro:<br/>
<ul>
<li>Mensajes de estado</li>
<li>Advertencias no graves</li>
<li>Todos los mensajes de error</li>
<li>Inicio de acciones</li>
<li>Registros específicos de la acción</li>
<li>Solicitudes de usuario</li>
<li>Parámetros iniciales de la interfaz de usuario</li>
<li>Memoria insuficiente o información de salida irrecuperable</li>
<li>Mensajes de espacio insuficiente en disco</li>
<li>Propiedades de terminal</li>
</ul>
<blockquote>
[!Note]<br />
La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/l *</strong>.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Para obtener más información acerca de todos los métodos que están disponibles para establecer el modo de registro, consulte el <a href="normal-logging.md">registro normal</a> en la sección <a href="windows-installer-logging.md">registro de Windows Installer</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/Package</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Opción instalar producto. Instala o configura un producto.<br/>
<blockquote>
[!Note]<br />
La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/i</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Update</strong></td>
<td><em><Update1.msp>[; Update2. MSP]</em></td>
<td>Opción instalar revisiones. Instala una o varias revisiones. <br/>
<blockquote>
[!Note]<br />
La línea de comandos de Windows Installer equivalente tiene <a href="patch.md"><strong>patch</strong></a> = [msipatch. msp] <; PatchGuid2> establece en la línea de comandos.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
