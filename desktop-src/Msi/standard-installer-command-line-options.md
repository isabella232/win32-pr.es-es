---
description: el programa ejecutable que interpreta paquetes e instala productos es Msiexec.exe. Tenga en cuenta que Msiexec también establece un nivel de error en la devolución que corresponde a los códigos de error del sistema. En la tabla siguiente se identifican las opciones de línea de comandos estándar para este programa. Las opciones de línea de comandos no tienen en cuenta las mayúsculas y minúsculas. Windows Instalador 2.0: las opciones de línea de comandos que se identifican en este tema están disponibles a partir de Windows Installer 3.0. Las Windows del instalador de Command-Line están disponibles con Windows Installer \#&160;3.0 y versiones anteriores.
ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018
---

# <a name="standard-installer-command-line-options"></a>Opciones de configuración Command-Line instalador estándar

El programa ejecutable que interpreta paquetes e instala productos es Msiexec.exe.

> [!Note]  
> Msiexec también establece un nivel de error en la devolución que corresponde a los [códigos de error del sistema](../debug/system-error-codes.md).

 

En la tabla siguiente se identifican las opciones de línea de comandos estándar para este programa. Las opciones de línea de comandos no tienen en cuenta las mayúsculas y minúsculas.

**Windows Installer 2.0:** Las opciones de línea de comandos que se identifican en este tema están disponibles a partir Windows Installer 3.0. Las Windows línea [de comandos](command-line-options.md) del instalador de aplicaciones están disponibles con Windows Installer 3.0 y versiones anteriores.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Ayuda y opción de referencia rápida. Muestra el uso correcto del comando de instalación, incluida una lista de todos los modificadores y el comportamiento. La descripción del uso se puede mostrar en la interfaz de usuario. El uso incorrecto de cualquier opción invoca esta opción de ayuda.<br/> Ejemplo: <strong>msiexec /help</strong><br/>
<blockquote>
[!Note]<br />
El equivalente Windows línea <a href="command-line-options.md">de comandos del instalador</a> es <strong>/?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Opción de visualización silenciosa. El instalador ejecuta una instalación sin mostrar una interfaz de usuario. No se muestran mensajes, mensajes ni cuadros de diálogo al usuario. El usuario no puede cancelar la instalación. Use las opciones de línea de comandos estándar <strong>/norestart</strong> <strong>o /forcerestart</strong> estándar para controlar los reinicios. Si no se especifica ninguna opción de reinicio, el instalador reinicia el equipo siempre que sea necesario sin mostrar ningún mensaje o advertencia al usuario.<br/> Ejemplos: <br/> <strong>msiexec /package Application.msi /quiet</strong><br/> <strong>Msiexec /uninstall Application.msi /quiet</strong><br/> <strong>Msiexec /update msipatch.msp /quiet</strong><br/> <strong>Msiexec /uninstall msipatch.msp /package Application.msi /quiet</strong><br/>
<blockquote>
[!Note]<br />
El equivalente Windows línea <a href="command-line-options.md">de comandos del instalador</a> es <strong>/qn</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>Opción de visualización pasiva. El instalador muestra una barra de progreso al usuario que indica que una instalación está en curso, pero no se muestran mensajes de error ni mensajes de error al usuario. El usuario no puede cancelar la instalación. Use las opciones de línea de comandos estándar <strong>/norestart</strong> <strong>o /forcerestart</strong> estándar para controlar los reinicios. Si no se especifica ninguna opción de reinicio, el instalador reinicia el equipo siempre que sea necesario sin mostrar ningún mensaje o advertencia al usuario. <br/> Ejemplo: <strong>msiexec /package Application.msi /passive</strong> <br/>
<blockquote>
[!Note]<br />
El equivalente Windows <a href="command-line-options.md">línea</a> de comandos del instalador es <strong>/qb!-</strong> con <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S establecido en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Opción No reiniciar nunca. El instalador nunca reinicia el equipo después de la instalación.<br/> Ejemplo: msiexec /package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
El equivalente Windows línea de comandos del instalador <a href="reboot.md"><strong>tiene REBOOT</strong></a>=ReallySuppress establecido en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>Opción reiniciar siempre. El instalador siempre reinicia el equipo después de cada instalación.<br/> Ejemplo: msiexec /package Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
El equivalente Windows línea de comandos del instalador tiene <a href="reboot.md"><strong>REBOOT</strong></a>=Force establecido en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Preguntar antes de reiniciar la opción. Muestra un mensaje que indica que se requiere un reinicio para completar la instalación y pregunta al usuario si debe reiniciar el sistema ahora. Esta opción no se puede usar junto con <strong>la opción /quiet.</strong><br/>
<blockquote>
[!Note]<br />
La línea de comandos Windows installer equivalente tiene <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; establecido en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/uninstall</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Opción Desinstale el producto. Desinstala un producto.<br/>
<blockquote>
[!Note]<br />
El equivalente Windows línea <a href="command-line-options.md">de comandos del instalador</a> es <strong>/x</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/uninstall</strong></td>
<td><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1> [; Update2.msp | PatchGUID2]</em></td>
<td>Opción de actualización de desinstalación. Desinstala una revisión de actualización.<br/>
<blockquote>
[!Note]<br />
La opción Windows <a href="command-line-options.md">línea</a> de comandos del instalador equivalente es <strong>/I</strong> <a href="msipatchremove.md"><strong>con MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[; Update2.msp | PatchGUID2] se establece en la línea de comandos.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Opción de registro. Escribe información de registro en un archivo de registro en la ruta de acceso existente especificada. La ruta de acceso a la ubicación del archivo de registro ya debe existir. El instalador no crea la estructura de directorios para el archivo de registro.<br/> La siguiente información se introduce en el registro:<br/>
<ul>
<li>Mensajes de estado</li>
<li>Advertencias nofatales</li>
<li>Todos los mensajes de error</li>
<li>Inicio de acciones</li>
<li>Registros específicos de la acción</li>
<li>Solicitudes de usuario</li>
<li>Parámetros iniciales de la interfaz de usuario</li>
<li>Información de salida irresal o de memoria</li>
<li>Mensajes de espacio fuera del disco</li>
<li>Propiedades del terminal</li>
</ul>
<blockquote>
[!Note]<br />
El equivalente Windows línea <a href="command-line-options.md">de comandos del instalador</a> es <strong>/L*.</strong>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Para obtener más información sobre todos los métodos que están disponibles para establecer el modo de registro, vea <a href="normal-logging.md">Registro normal</a> en la <a href="windows-installer-logging.md">Windows registro</a> del instalador.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/package</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Instalación de la opción de producto. Instala o configura un producto.<br/>
<blockquote>
[!Note]<br />
El equivalente Windows línea <a href="command-line-options.md">de comandos del instalador</a> es <strong>/I</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/update</strong></td>
<td><em><Update1.msp>[; Update2.msp]</em></td>
<td>Opción Instalar revisiones. Instala una o varias revisiones. <br/>
<blockquote>
[!Note]<br />
La línea de comandos Windows Installer equivalente tiene <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<; PatchGuid2> en la línea de comandos.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
