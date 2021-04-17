---
description: Opciones de línea de comandos para msiexec.exe para Windows Installer 3,0 y versiones anteriores. Proporciona una tabla que muestra las opciones, los parámetros y las descripciones. Ejemplos que muestran cómo instalar productos y otras tareas.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Opciones de la línea de comandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fe56026c21e4120963c86b4de08decc85b2a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652893"
---
# <a name="command-line-options"></a>Opciones de la línea de comandos

El programa ejecutable que interpreta paquetes e instala productos es Msiexec.exe. Tenga en cuenta que msiexec también establece un nivel de error en la devolución que corresponde a los [códigos de error del sistema](/windows/desktop/Debug/system-error-codes). Las opciones de línea de comandos no distinguen mayúsculas de minúsculas.

Las opciones de línea de comandos de la tabla siguiente están disponibles con Windows Installer 3,0 y versiones anteriores. El [instalador estándar Command-Line opciones](standard-installer-command-line-options.md) también están disponibles a partir de Windows Installer 3,0.



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
<td><strong>/I</strong></td>
<td><em>Paquete | ProductCode</em></td>
<td>Instala o configura un producto.<br/></td>
</tr>
<tr class="even">
<td><strong>/f</strong></td>
<td>[p | o | e | d | c | a | u | m | s | v] <em>Paquete</em> | de <em>ProductCode</em></td>
<td>Repara un producto. Esta opción omite los valores de propiedad especificados en la línea de comandos. La lista de argumentos predeterminada para esta opción es ' OMUs '. Esta opción comparte la misma lista de argumentos que la propiedad <a href="reinstallmode.md"><strong>REINSTALLMODE</strong></a> .<br/> p: vuelve a instalar solo si falta el archivo.<br/> o-vuelve a instalar si falta el archivo o si se ha instalado una versión anterior.<br/> e-reinstala si falta el archivo o si está instalada una versión igual o anterior.<br/> d: vuelve a instalar si falta el archivo o si se ha instalado una versión diferente.<br/> c: vuelve a instalar si falta el archivo o la suma de comprobación almacenada no coincide con el valor calculado. Solo repara archivos que tienen <strong>msidbFileAttributesChecksum</strong> en la columna Attributes de la tabla <a href="file-table.md">File</a> .<br/> a: fuerza la reinstalación de todos los archivos.<br/> u-reescribe todas las entradas necesarias del registro específicas del usuario.<br/> m: reescribe todas las entradas de registro específicas del equipo necesarias.<br/> s: Sobrescribe todos los accesos directos existentes.<br/> v: ejecuta desde el origen y vuelve a almacenar en caché el paquete local. No use la opción <strong>v</strong> REINSTALL para la primera instalación de una aplicación o característica.<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>Package</em></td>
<td>Opción de <a href="administrative-installation.md">instalación administrativa</a> . Instala un producto en la red.<br/></td>
</tr>
<tr class="even">
<td><strong>/x</strong></td>
<td><em>Paquete | ProductCode</em></td>
<td>Desinstala un producto.</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u | m] <em>Paquete</em> de<br/> [u | m] <em>Paquete</em><strong>/t</strong>,<em>lista de transformación</em><br/> <em>or</em><br/> [u | m] <em>Paquete</em><strong>/g</strong><em>iddeidioma</em><br/></td>
<td>Anuncia un producto. Esta opción omite los valores de propiedad especificados en la línea de comandos.<br/> u: anuncia al usuario actual.<br/> m: anuncia a todos los usuarios de la máquina.<br/> identificador de idioma g.<br/> t: aplica la transformación al paquete anunciado.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i | w | e | a | r | u | c | m | o | p | v | x | + |! | *] Archivo de <em>registro</em></td>
<td>Escribe información de registro en un archivo de registro en la ruta de acceso existente especificada. La ruta de acceso a la ubicación del archivo de registro ya debe existir. El instalador no crea la estructura de directorios para el archivo de registro. Las marcas indican la información que se va a registrar. Si no se especifican marcas, el valor predeterminado es ' iwearmo '.<br/> i: mensajes de estado.<br/> w: advertencias no graves.<br/> e: todos los mensajes de error.<br/> a: Inicio de acciones.<br/> r: registros específicos de la acción.<br/> solicitudes de u-usuario.<br/> c: parámetros iniciales de la interfaz de usuario.<br/> m-memoria insuficiente o información de salida irrecuperable.<br/> mensajes de espacio insuficiente en disco.<br/> propiedades de p-terminal.<br/> salida de v-Verbose.<br/> x: información de depuración adicional. <strong>Windows Installer 2,0:</strong> No compatible. La opción x está disponible con Windows Installer versión 3.0.3790.2180 y versiones posteriores.<br/> <br/> + - Anexar al archivo existente.<br/> ! -Vacíe cada línea en el registro.<br/> &quot;*&quot; -Comodín, registrar toda la información excepto las opciones v y x. Para incluir las opciones v y x, especifique &quot; /l* VX &quot; .<br/>
<blockquote>
[!Note]<br />
Para obtener más información acerca de todos los métodos disponibles para establecer el modo de registro, consulte <a href="normal-logging.md">registro normal</a> en la sección <a href="windows-installer-logging.md">registro de Windows Installer</a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/m</strong></td>
<td><em>extensión</em>
<blockquote>
[!Note]<br />
La longitud del <em>nombre de archivo</em> no debe tener más de ocho caracteres.
</blockquote>
<br/></td>
<td>Genera un archivo. MIF de estado de SMS. Debe usarse con las opciones instalar (-i), quitar (-x), instalación administrativa (-a) o reinstalar (-f). El ISMIF32.DLL se instala como parte de SMS y debe estar en la ruta de acceso.<br/> Los campos del archivo MIF de estado se rellenan con la información siguiente:<br/> Fabricante- <a href="author-summary.md"> <strong>autor</strong></a><br/> Producto- <a href="revision-number-summary.md"> <strong>número de revisión</strong></a><br/> Versión: <a href="subject-summary.md"> <strong>asunto</strong></a><br/> Configuración regional: <a href="template-summary.md"> <strong>plantilla</strong></a><br/> Número de serie: no establecido<br/> Instalación: establecida por ISMIF32.DLL en &quot; DateTime&quot;<br/> InstallStatus: &quot; correcto &quot; o con &quot; errores&quot;<br/> Descripción: mensajes de error en el siguiente orden: 1) mensajes de error generados por el instalador. 2) recurso de Msi.dll si la instalación no pudo iniciar o salir del usuario. 3) archivo de mensajes de error del sistema. 4) mensaje con formato: &quot; error del instalador% i &quot; , donde se ha devuelto un error de Msi.dll.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PatchPackage [;P atchpackage2</em> ]</td>
<td>Aplica una revisión. Para aplicar una revisión a una imagen administrativa instalada, debe combinar las siguientes opciones:<br/> /p <em> <PatchPackage> [;p atchpackage2] </em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n | b | r | f</td>
<td>Establece el <a href="user-interface-levels.md">nivel de interfaz de usuario</a>.<br/> q, QN-sin interfaz de usuario<br/> QB: <a href="b-gly.md"><em>interfaz de usuario básica</em></a>. Use QB! para ocultar el botón <strong>Cancelar</strong> .<br/> QR: <a href="r-gly.md"><em>interfaz de usuario reducida</em></a> sin cuadro de diálogo modal mostrado al final de la instalación.<br/> QF: <a href="f-gly.md"><em>interfaz de usuario completa</em></a> y todos los cuadros de diálogo modales de <a href="fatalerror-dialog.md">FatalError</a>, <a href="userexit-dialog.md">UserExit</a>o <a href="exit-dialog.md">Exit</a> al final.<br/> QN +-sin interfaz de usuario excepto para un cuadro de diálogo modal que se muestra al final.<br/> QB +: <a href="b-gly.md"><em>interfaz de usuario básica</em></a> con un cuadro de diálogo modal que se muestra al final. No se muestra el cuadro modal si el usuario cancela la instalación. Use QB +! o QB! + para ocultar el botón <strong>Cancelar</strong> .<br/> QB: <a href="b-gly.md"><em>interfaz de usuario básica</em></a> sin cuadros de diálogo modales. Tenga en cuenta que/QB +-no es un nivel de interfaz de usuario admitido. Use QB-! o QB!-para ocultar el botón <strong>Cancelar</strong> .<br/> Tenga en cuenta que el la opción está disponible con Windows Installer 2,0 y solo funciona con la interfaz de usuario básica. No es válido con la interfaz de usuario completa.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> o <strong>/h</strong></td>
<td> </td>
<td>Muestra información de copyright para Windows Installer.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>destina</em></td>
<td>Llama a la función del sistema <strong>DllRegisterServer</strong> para registrar automáticamente los módulos pasados en la línea de comandos. Especifique la ruta de acceso completa al archivo DLL. Por ejemplo, para MY_FILE.DLL en la carpeta actual, puede usar:<br/> <strong>msiexec/y .\MY_FILE.DLL</strong><br/> Esta opción solo se utiliza para la información del registro que no se puede agregar mediante las tablas del registro del archivo. msi.<br/></td>
</tr>
<tr class="even">
<td><strong>/z</strong></td>
<td><em>destina</em></td>
<td>Llama a la función del sistema <strong>DllUnregisterServer</strong> para eliminar del registro los módulos pasados en la línea de comandos. Especifique la ruta de acceso completa al archivo DLL. Por ejemplo, para MY_FILE.DLL en la carpeta actual, puede usar: <br/> <strong>msiexec/z .\MY_FILE.DLL</strong><br/> Esta opción solo se utiliza para la información del registro que no se puede quitar mediante las tablas del registro del archivo. msi.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Anuncia una nueva instancia del producto. Debe usarse junto con/t. Disponible a partir de la versión de Windows Installer que se incluye con Windows Server 2003 y Windows XP con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><strong>/n</strong></td>
<td><em>ProductCode</em></td>
<td>Especifica una instancia concreta del producto. Se usa para identificar una instancia de instalada mediante la compatibilidad con varias instancias a través de una transformación de cambio de código de producto. Disponible a partir de la versión de Windows Installer incluida con Windows Server 2003 y Windows XP con SP1. <br/></td>
</tr>
</tbody>
</table>



 

Las opciones/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| \| v s \] ,/j \[ u \| m \] ,/a,/p,/y y/z no deben usarse juntas. La única excepción a esta regla es que la revisión de una [instalación administrativa](administrative-installation.md) requiere el uso de/p y/a. Las opciones/t,/c y/g solo deben usarse con/j. Las opciones/l y/q se pueden usar con/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] ,/j \[ u \| m \] ,/a y/p. Se puede usar la opción/n con/i,/f,/x y/p.

Para instalar un producto desde un: \\Example.msi, instale el producto de la siguiente manera:

**msiexec/i A: \\Example.msi**

Solo se pueden modificar [las propiedades públicas](public-properties.md) mediante la línea de comandos. Todos los nombres de propiedad de la línea de comandos se interpretan como mayúsculas, pero el valor conserva la distinción de mayúsculas y minúsculas. Si escribe una **propiedad** en una línea de comandos, el instalador invalida el valor de propiedad y no el valor de la **propiedad** de la tabla de propiedades. Para obtener más información, vea [acerca de las propiedades](about-properties.md).

Para instalar un producto con la propiedad establecida en valor, use la siguiente sintaxis en la línea de comandos. Puede colocar la propiedad en cualquier lugar excepto entre una opción y su argumento.

Sintaxis correcta:

**msiexec/i A: \\Example.msi propiedad = valor**

Sintaxis incorrecta:

**msiexec/i PROPERTY = valor A: \\Example.msi**

Los valores de propiedad que son cadenas literales deben ir entre comillas. Incluya los espacios en blanco de la cadena entre las marcas.

**msiexec/i A: \\Example.msi propiedad = "espacio en blanco incrustado"**

Para borrar una propiedad pública mediante la línea de comandos, establezca su valor en una cadena vacía.

**msiexec/i A: \\Example.msi propiedad = ""**

En el caso de las secciones de texto separadas por Comillas literales, incluya la sección con un segundo par de Comillas.

**msiexec/i A: \\Example.msi propiedad = "" comillas "incrustado" "espacio en blanco"**

En el ejemplo siguiente se muestra una línea de comandos complicada.

**msiexec/i testdb.msi INSTALLLEVEL = 3/l \* MSI. log CompanyName = "Acme" "widgets" "y" "Gizmos" "**

En el ejemplo siguiente se muestran las opciones de anuncio. Tenga en cuenta que los modificadores no distinguen mayúsculas de minúsculas.

**msiexec/JM msisample.msi/T transform. MST/LIME logfile.txt**

En el ejemplo siguiente se muestra cómo instalar una nueva instancia de un producto que se va a anunciar. Este producto se creó para admitir varias transformaciones de instancias.

**msiexec/JM msisample.msi/T: Instance1. MST; Customization. MST/c/LIME logfile.txt**

En el ejemplo siguiente se muestra cómo aplicar una revisión a una instancia de un producto que se instala mediante transformaciones de varias instancias.

**msiexec/p msipatch. MSP; msipatch2. MSP/n {00000001-0002-0000-0000-624474736554} /qb**

Al aplicar revisiones a un producto específico, las opciones/i y/p no se pueden especificar juntas en una línea de comandos. En este caso, puede aplicar revisiones a un producto como se indica a continuación.

**msiexec/i A: \\Example.msi patch = msipatch. MSP; msipatch2. MSP/QB**

No se puede establecer la propiedad [**patch**](patch.md) en una línea de comandos, cuando se usa la opción/p. Si se establece la propiedad **patch** cuando se usa la opción/p, se omite y se sobrescribe el valor de la propiedad **patch** .

 

