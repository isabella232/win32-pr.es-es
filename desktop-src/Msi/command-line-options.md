---
description: Opciones de línea de comandos msiexec.exe para Windows Installer 3.0 y versiones anteriores. Proporciona una tabla que muestra opciones, parámetros y descripciones. Ejemplos que muestran cómo instalar productos y otras tareas.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Opciones de la línea de comandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72592046bdd30429d373f23f1d2cb39bc9497ee
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630911"
---
# <a name="command-line-options"></a>Opciones de la línea de comandos

El programa ejecutable que interpreta paquetes e instala productos es Msiexec.exe. Tenga en cuenta que Msiexec también establece un nivel de error en la devolución que corresponde a los [códigos de error del sistema](/windows/desktop/Debug/system-error-codes). Las opciones de la línea de comandos no tienen en cuenta las mayúsculas y minúsculas.

Las opciones de línea de comandos de la tabla siguiente están disponibles con Windows Installer 3.0 y versiones anteriores. Las [opciones de configuración Command-Line instalador](standard-installer-command-line-options.md) estándar también están disponibles a partir de Windows Installer 3.0.



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
<td><strong>/I</strong></td>
<td><em>Paquete| Productcode</em></td>
<td>Instala o configura un producto.<br/></td>
</tr>
<tr class="even">
<td><strong>/f</strong></td>
<td>[p|o|e|d|c|a|u|m|s|v] <em>Paquete</em> | <em>ProductCode</em></td>
<td>Repara un producto. Esta opción omite los valores de propiedad especificados en la línea de comandos. La lista de argumentos predeterminada para esta opción es "omus". Esta opción comparte la misma lista de argumentos que la <a href="reinstallmode.md"><strong>propiedad REINSTALLMODE.</strong></a><br/> p: se vuelve a instalar solo si falta el archivo.<br/> o: se vuelve a instalar si falta el archivo o si hay instalada una versión anterior.<br/> e: se vuelve a instalar si falta el archivo o si hay instalada una versión igual o anterior.<br/> d : se vuelve a instalar si falta el archivo o si hay instalada una versión diferente.<br/> c: se vuelve a instalar si falta el archivo o la suma de comprobación almacenada no coincide con el valor calculado. Solo repara los archivos que tienen <strong>msidbFileAttributesChecksum</strong> en la columna Atributos de la <a href="file-table.md">tabla File.</a><br/> a : fuerza la reinstalación de todos los archivos.<br/> u: reescribe todas las entradas del Registro específicas del usuario necesarias.<br/> m: reescribe todas las entradas del Registro específicas del equipo necesarias.<br/> s: sobrescribe todos los accesos directos existentes.<br/> v: se ejecuta desde el origen y vuelve a almacenar en caché el paquete local. No use la opción <strong>v</strong> reinstall para la primera instalación de una aplicación o característica.<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>Paquete</em></td>
<td><a href="administrative-installation.md">Opción de instalación</a> administrativa. Instala un producto en la red.<br/></td>
</tr>
<tr class="even">
<td><strong>/x</strong></td>
<td><em>Paquete| Productcode</em></td>
<td>Desinstala un producto.</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u|m] <em>Empaquetador</em><br/> [u|m] <em>Package</em><strong>/t</strong><em>Transform List</em><br/> <em>or</em><br/> [u|m] <em>Package</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>Anuncia un producto. Esta opción omite los valores de propiedad especificados en la línea de comandos.<br/> u: anuncia al usuario actual.<br/> m: anuncia a todos los usuarios de la máquina.<br/> g: identificador de idioma.<br/> t: aplica la transformación al paquete anunciado.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i|w|e|a|r|u|c|m|o|p|v|x|+|!| *] <em>Archivo de registro</em></td>
<td>Escribe información de registro en un archivo de registro en la ruta de acceso existente especificada. La ruta de acceso a la ubicación del archivo de registro ya debe existir. El instalador no crea la estructura de directorios para el archivo de registro. Las marcas indican qué información se va a registrar. Si no se especifica ninguna marca, el valor predeterminado es "iandermo".<br/> i: mensajes de estado.<br/> w : advertencias nofatales.<br/> e: todos los mensajes de error.<br/> a : inicio de acciones.<br/> r: registros específicos de la acción.<br/> u : solicitudes de usuario.<br/> c: parámetros iniciales de la interfaz de usuario.<br/> m: información de salida irresal o de memoria no útil.<br/> o: mensajes de espacio fuera del disco.<br/> p: propiedades de terminal.<br/> v: salida detallada.<br/> x: información de depuración adicional. <strong>Windows Installer 2.0:</strong> No se admite. La opción x está disponible con Windows Installer versión 3.0.3790.2180 y posteriores.<br/> <br/> + - Anexe al archivo existente.<br/> ! - Vacíe cada línea al registro.<br/> &quot;*&quot; - Comodín, registre toda la información excepto las opciones v y x. Para incluir las opciones v y x, especifique &quot; /l* vx &quot; .<br/>
<blockquote>
[!Note]<br />
Para obtener más información sobre todos los métodos que están disponibles para establecer el modo de registro, vea <a href="normal-logging.md">Registro normal</a> en la sección Registro <a href="windows-installer-logging.md">Windows instalador.</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/m</strong></td>
<td><em>Nombre</em>
<blockquote>
[!Note]<br />
La longitud del <em>nombre de</em> archivo no debe tener más de ocho caracteres.
</blockquote>
<br/></td>
<td>Genera un archivo .mif de estado de SMS. Debe usarse con las opciones de instalación (-i), eliminación (-x), instalación administrativa (-a) o reinstalación (-f). El ISMIF32.DLL se instala como parte de SMS y debe estar en la ruta de acceso.<br/> Los campos del archivo mif de estado se rellenan con la siguiente información:<br/> Fabricante: <a href="author-summary.md"> <strong>autor</strong></a><br/> Producto: número <a href="revision-number-summary.md"> <strong>de revisión</strong></a><br/> Versión: <a href="subject-summary.md"> <strong>asunto</strong></a><br/> Configuración regional: <a href="template-summary.md"> <strong>plantilla</strong></a><br/> Número de serie: no establecido<br/> Instalación: se establece ISMIF32.DLL en &quot; DateTime&quot;<br/> InstallStatus: &quot; correcto o con &quot; &quot; errores&quot;<br/> Descripción: mensajes de error en el orden siguiente: 1) Mensajes de error generados por el instalador. 2) Recurso de Msi.dll si no se pudo iniciar la instalación o si el usuario no pudo salir. 3) Archivo de mensaje de error del sistema. 4) Mensaje con formato: &quot; error del instalador &quot; %i, donde %i es un error devuelto desde Msi.dll.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PatchPackage[;p atchPackage2</em> ]</td>
<td>Aplica una revisión. Para aplicar una revisión a una imagen administrativa instalada, debe combinar las siguientes opciones:<br/> /p <em> <PatchPackage> [;p atchPackage2 ] </em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n|b|r|f</td>
<td>Establece el <a href="user-interface-levels.md">nivel de interfaz de usuario</a>.<br/> q, qn- Sin interfaz de usuario<br/> qb: interfaz <a href="b-gly.md"><em>de usuario básica.</em></a> Use qb! para ocultar el <strong>botón</strong> Cancelar.<br/> qr: <a href="r-gly.md"><em>interfaz de usuario</em></a> reducida sin cuadro de diálogo modal mostrado al final de la instalación.<br/> plot: <a href="f-gly.md"><em>interfaz de</em></a> usuario completa y cualquier cuadro de diálogo modal <a href="fatalerror-dialog.md">FatalError</a>, <a href="userexit-dialog.md">UserExit</a>o <a href="exit-dialog.md">Exit</a> al final.<br/> qn+: no hay interfaz de usuario excepto un cuadro de diálogo modal que se muestra al final.<br/> qb+: <a href="b-gly.md"><em>interfaz de usuario básica</em></a> con un cuadro de diálogo modal mostrado al final. El cuadro modal no se muestra si el usuario cancela la instalación. Use qb+! o qb!+ para ocultar el <strong>botón</strong> Cancelar.<br/> qb- - <a href="b-gly.md"><em>Interfaz de usuario básica</em></a> sin cuadros de diálogo modales. Tenga en cuenta que /qb+- no es un nivel de interfaz de usuario compatible. Uso de qb-! o qb!- para ocultar el <strong>botón</strong> Cancelar.<br/> Tenga en cuenta que ! La opción está disponible con Windows Installer 2.0 y solo funciona con la interfaz de usuario básica. No es válido con la interfaz de usuario completa.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> o <strong>/h</strong></td>
<td> </td>
<td>Muestra información de copyright de Windows Installer.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>Módulo</em></td>
<td>Llama a la función del <strong>sistema DllRegisterServer para</strong> registrar automáticamente los módulos pasados en la línea de comandos. Especifique la ruta de acceso completa al archivo DLL. Por ejemplo, para MY_FILE.DLL en la carpeta actual puede usar:<br/> <strong>msiexec /y .\MY_FILE.DLL</strong><br/> Esta opción solo se usa para la información del Registro que no se puede agregar mediante las tablas del Registro .msi archivo.<br/></td>
</tr>
<tr class="even">
<td><strong>/z</strong></td>
<td><em>Módulo</em></td>
<td>Llama a la función del <strong>sistema DllUnRegisterServer para</strong> anular el registro de los módulos pasados en la línea de comandos. Especifique la ruta de acceso completa al archivo DLL. Por ejemplo, para MY_FILE.DLL en la carpeta actual puede usar: <br/> <strong>msiexec /z .\MY_FILE.DLL</strong><br/> Esta opción solo se usa para la información del Registro que no se puede quitar mediante las tablas del Registro del .msi archivo.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Anuncia una nueva instancia del producto. Debe usarse junto con /t. Disponible a partir de Windows Installer que se incluye con Windows Server 2003 y Windows XP con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><strong>/n</strong></td>
<td><em>ProductCode</em></td>
<td>Especifica una instancia determinada del producto. Se usa para identificar una instancia instalada mediante la compatibilidad con varias instancias a través de un código de producto que cambia las transformaciones. Disponible a partir de Windows Installer incluido con Windows Server 2003 y Windows XP con SP1. <br/></td>
</tr>
</tbody>
</table>



 

Las opciones /i, /x, /f \[ p o e d c a u m s \| v \| , \| \| \| \| \| \| \| \] /j u m , \[ \| \] /a, /p, /y y /z no deben usarse juntas. La única excepción a esta regla es que la aplicación de revisiones a una [instalación administrativa](administrative-installation.md) requiere el uso de /p y /a. Las opciones /t, /c y /g solo se deben usar con /j. Las opciones /l y /q se pueden usar con /i, /x, /f \[ p o e d c a u m s \| v \| , \| \| \| \| \| \| \| \] /j u m , \[ \| \] /a y /p. La opción /n se puede usar con /i, /f, /x y /p.

Para instalar un producto desde A: \\Example.msi, instale el producto como se muestra a continuación:

**msiexec /i A: \\Example.msi**

Solo [las propiedades públicas](public-properties.md) se pueden modificar mediante la línea de comandos. Todos los nombres de propiedad de la línea de comandos se interpretan en mayúsculas, pero el valor conserva la confidencialidad de mayúsculas y minúsculas. Si escribe **MyProperty en una** línea de comandos, el instalador invalida el valor de MYPROPERTY y no el valor de **MyProperty** en la tabla Property. Para obtener más información, vea [Acerca de las propiedades](about-properties.md).

Para instalar un producto con PROPERTY establecido en VALUE, use la siguiente sintaxis en la línea de comandos. Puede colocar la propiedad en cualquier lugar excepto entre una opción y su argumento.

Sintaxis correcta:

**msiexec /i A: \\Example.msi PROPERTY=VALUE**

Sintaxis incorrecta:

**msiexec /i PROPERTY=VALUE A: \\Example.msi**

Los valores de propiedad que son cadenas literales deben ir entre comillas. Incluya los espacios en blanco de la cadena entre las marcas.

**msiexec /i A: \\Example.msi PROPERTY="Embedded White Space"**

Para borrar una propiedad pública mediante la línea de comandos, establezca su valor en una cadena vacía.

**msiexec /i A: \\Example.msi PROPERTY=""**

Para las secciones de texto separadas por comillas literales, incluya la sección con un segundo par de comillas.

**msiexec /i A: \\Example.msi PROPERTY="Embedded ""Quotes"" White Space"**

En el ejemplo siguiente se muestra una línea de comandos complicada.

**msiexec /i testdb.msi INSTALLLEVEL=3 /l \* msi.log COMPANYNAME="Acme ""Widgets"" y ""Gizmos."""**

En el ejemplo siguiente se muestran las opciones de anuncio. Tenga en cuenta que los modificadores no distinguen mayúsculas de minúsculas.

**msiexec /JM msisample.msi /T transform.mst /LIME logfile.txt**

En el ejemplo siguiente se muestra cómo instalar una nueva instancia de un producto que se va a anunciar. Este producto se ha escrito para admitir varias transformaciones de instancia.

**msiexec /JM msisample.msi /T :instance1.mst;customization.mst /c /LIME logfile.txt**

En el ejemplo siguiente se muestra cómo aplicar revisiones a una instancia de un producto que se instala mediante varias transformaciones de instancia.

**msiexec /p msipatch.msp;msipatch2.msp /n {00000001-0002-0000-0000-624474736554} /qb**

Al aplicar revisiones a un producto específico, las opciones /i y /p no se pueden especificar juntas en una línea de comandos. En este caso, puede aplicar revisiones a un producto como se muestra a continuación.

**msiexec /i A: \\Example.msi PATCH=msipatch.msp;msipatch2.msp /qb**

La [**propiedad PATCH**](patch.md) no se puede establecer en una línea de comandos cuando se usa la opción /p. Si la **propiedad PATCH** se establece cuando se usa la opción /p, el valor de la **propiedad PATCH** se omite y se sobrescribe.

 

