---
description: El archivo Mt.exe es una herramienta que genera archivos y catálogos firmados. Está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows. Mt.exe requiere que el archivo al que se hace referencia en el manifiesto esté presente en el mismo directorio que el manifiesto.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df654a943bad272a091dc6ac20cc1dcdab1731a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652357"
---
# <a name="mtexe"></a>Mt.exe

El archivo Mt.exe es una herramienta que genera archivos y catálogos firmados. Está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows. Mt.exe requiere que el archivo al que se hace referencia en el manifiesto esté presente en el mismo directorio que el manifiesto.

Mt.exe genera hashes mediante la implementación de CryptoAPI del algoritmo hash seguro (SHA-1). Para obtener más información sobre los algoritmos hash, vea [algoritmos hash y de firma](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Los valores hash se insertan como una cadena hexadecimal en las etiquetas de **archivo** del manifiesto. Actualmente, la herramienta solo genera hashes SHA-1, aunque los archivos de los manifiestos pueden usar otros esquemas hash.

Mt.exe usa Makecat.exe para generar archivos de catálogo (. cat) a partir de archivos de definición de catálogo (. CDF). Esta herramienta rellena un CDF de plantilla estándar con el nombre y la ubicación del manifiesto. Puede utilizarlo con Makecat.exe para generar el catálogo de ensamblados.

La versión de Mt.exe que se proporciona en las versiones recientes del Windows SDK también puede usarse para generar manifiestos para ensamblados administrados y ensamblados simultáneos no administrados.

## <a name="syntax"></a>Sintaxis

**mt.exe \[ -manifest** _<component1. manifest><component2. manifest>_ *_\] \[ -Identity:_* *<identity string> * **\] \[ -RGS:** _<archivo1. RGS>_* _\] \[ -tlb:_ *_<archivo2. tlb>_* _\] \[ -dll:_ *_<_* file3.dll>_\] \[ -replaces:_ *_<XML filename>_* _\] \[ -managedassemblyname:_ *_<managed assembly>_* _\] \[ -nodependency \] \[ -Category \] \[ -out:_ *_<output manifest name>_* _\] \[ -inputresource:_ *_<file4>_* _; \[ \# \]_ *_><0 \_ ID. de recurso><1_* _\] \[ -outputresource:_ *_<file5>_* _; \[ \# \]_ *_><2 \_ ID. de recurso><3_* _\] \[ -updateresource:_ *_<file6>_* _; \[ \# \]_ *_><4 \_ ID. de recurso><5_* _\] \[ -hashupdate \[ :_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -Validate \_ manifiesto \] \[ -validar \_ hash de \__ *_<path to files>_* _\] \[ \] \[ \_ \_ \] \[ \] \[ archivo:-canonizar-comprobar para duplicados-nologo-verbose \]_*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Mt.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-manifest</td>
<td>Especifica el nombre del archivo de manifiesto. Para modificar un solo manifiesto, especifique un nombre de archivo de manifiesto. Por ejemplo, Component. manifest.<br/> Para combinar varios manifiestos, especifique aquí los nombres de los manifiestos de origen. Especifique el nombre del manifiesto actualizado con las opciones <strong>-out</strong>, <strong>-outputresource</strong>o <strong>-updateresource</strong> . Por ejemplo, la siguiente línea de comandos solicita una operación que combina dos manifiestos, man1. manifest y MAN2. manifest, en un nuevo manifiesto, man3. manifest.<br/> <strong>mt.exe-manifest man1. manifest MAN2. manifest-out: man3. manifest</strong><br/>
<blockquote>
[!Note]<br />
Sin dos puntos (:) se requiere con la opción <strong>-manifest</strong> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-Identity</td>
<td>Proporciona los valores de los atributos del elemento <strong>assemblyIdentity</strong> del manifiesto. El argumento de la opción <strong>-Identity</strong> es un valor de cadena que contiene los valores de atributo en campos separados por comas. Proporcione el valor del atributo de <strong>nombre</strong> en el primer campo, sin incluir un &quot; nombre = &quot; subcadena. Todos los campos restantes especifican los atributos y sus valores con el formato: <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Por ejemplo, para actualizar el elemento <strong>assemblyIdentity</strong> del manifiesto con la siguiente información:<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> incluya la siguiente opción <strong>-Identity</strong> en la línea de comandos:<br/> <strong>-Identity:</strong> &quot; Microsoft. Windows. SampleAssembly, processorArchitecture = x86, version = 6.0.0.0, Type = Win32, publicKeyToken = a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-RGS</td>
<td>Especifica el nombre del archivo de script de registro (. RGS). La opción <strong>-dll</strong> es necesaria para utilizar la opción <strong>-RGS</strong> .<br/></td>
</tr>
<tr class="even">
<td>-TLB</td>
<td>Especifica el nombre del archivo de biblioteca de tipos (.tlb). La opción <strong>-dll</strong> es necesaria para utilizar la opción <strong>-tlb</strong> .<br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>Especifica el nombre del archivo de biblioteca de vínculos dinámicos (DLL). <strong>mt.exe</strong> requiere la opción <strong>-dll</strong> si se usan las opciones <strong>-RGS</strong> o <strong>-tlb</strong> . Especifique el nombre del archivo DLL que desea compilar a partir de los archivos. RGS o. tlb.<br/> Por ejemplo, el comando siguiente solicita una operación que genera un manifiesto a partir de archivos. RGS y. tlb.<br/> <strong>mt.exe-RGS: testreg1. RGS-TLB: testlib1. tlb -dll:test.dll-replaces: REP. manifest-Identity: &quot; Microsoft. Windows. SampleAssembly, processorArchitecture = x86, version = 6.0.0.0, Type = Win32, PublicKeyToken = a5aaf5ba15723d5 &quot; -out: rgstlb. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-reemplazos</td>
<td>Especifica el archivo que contiene los valores para la cadena reemplazable en el archivo. RGS.<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>Genera un manifiesto del ensamblado administrado especificado. Se usa con la opción <strong>-nodependency</strong> para generar un manifiesto sin elementos de dependencia. Se usa con la opción <strong>-Category</strong> para generar un manifiesto con etiquetas de categoría. Por ejemplo, si managed.dll es un ensamblado administrado, la siguiente línea de comandos genera el manifiesto out desde managed.dll.<br/> <strong> Desmt.exe -managedassemblyname:managed.dll: out. manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-nodependency</td>
<td>Especifica una operación que genera un manifiesto sin elementos de dependencia. La opción <strong>-nodependency</strong> requiere la opción <strong>-managedassemblyname</strong> . Por ejemplo, si managed.dll es un ensamblado administrado, la siguiente línea de comandos genera el manifiesto out desde managed.dll sin información de dependencia.<br/> <strong> Desmt.exe -managedassemblyname:managed.dll: out. manifest-nodependency</strong><br/></td>
</tr>
<tr class="odd">
<td>-Categoría</td>
<td>Especifica una operación que genera un manifiesto con etiquetas de categoría. La opción <strong>-Category</strong> requiere la opción <strong>-managedassemblyname</strong> . Por ejemplo, si managed.dll es un ensamblado administrado, la siguiente línea de comandos genera el manifiesto out desde managed.dll con etiquetas de categoría.<br/> <strong>mt.exe -managedassemblyname:managed.dll: out. manifest-Category</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Especifica una operación que se ejecuta sin mostrar los datos de copyright de Microsoft estándar. Si <strong>mt.exe</strong> se ejecuta como parte de un proceso de compilación, esta opción se puede usar para evitar escribir información no deseada en los archivos de registro. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Especifica el nombre del manifiesto actualizado. Si se trata de una operación de un solo manifiesto y se omite la opción <strong>-out</strong> , se modifica el manifiesto original. <br/></td>
</tr>
<tr class="even">
<td>-inputresource</td>
<td>Especifica una operación realizada en un manifiesto Obtenido de un recurso de tipo RT_MANIFEST. Si se usa la opción <strong>-inputresource</strong> sin especificar el identificador de recursos, <em> <resource_id> </em> , la operación utiliza el valor CREATEPROCESS_MANIFEST_RESOURCE. <br/> Por ejemplo, el comando siguiente solicita una operación que combina un manifiesto de una DLL, dll_with_manifest.dll y un archivo de manifiesto, MAN2. manifest. Los manifiestos combinados los recibe un manifiesto en el archivo de recursos de otro archivo DLL, dll_with_merged_manifests. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll; #1-manifest MAN2. manifest -outputresource:dll_with_merged_manifest.dll; #3</strong><br/> Para extraer el manifiesto de un archivo DLL, especifique el nombre del archivo DLL. Por ejemplo, el comando siguiente extrae el manifiesto de lib1.dll y man3. manifest recibe el manifiesto extraído.<br/> <strong>mt.exe -inputresource:lib.dll; #1 de salida: man3. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>Especifica una operación que genera un manifiesto que recibirá un recurso de tipo RT_MANIFEST. Si se usa la opción <strong>-outputresource</strong> sin especificar el identificador de recursos, <em> <resource_id> </em> , la operación utiliza el valor CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-updateresource</td>
<td>Especifica una operación equivalente a usar las opciones <strong>-inputresource</strong> y <strong>-outputresource</strong> con argumentos idénticos. Por ejemplo, el comando siguiente solicita una operación que calcula un hash de los archivos en la ruta de acceso especificada y actualiza el manifiesto de un recurso de un archivo ejecutable portable (PE).<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll; #1-hashupdate: f: \files</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>Calcula el valor hash de los archivos en las rutas de acceso especificadas y actualiza el valor del atributo <strong>hash</strong> del elemento <strong>File</strong> con este valor. <br/> Por ejemplo, el comando siguiente solicita una operación que combina dos archivos de manifiesto, man1. manifest y MAN2. manifest, y actualiza el valor del atributo <strong>hash</strong> del elemento <strong>File</strong> del manifiesto que recibe la información combinada combinada. manifest.<br/> <strong>mt.exe-manifest man1. manifest MAN2. manifest-hashupdate: d: \filerepository-out: Merged. manifest</strong><br/> Si no se especifican las rutas de acceso a los archivos, la operación busca en la ubicación del manifiesto especificado para recibir la actualización. Por ejemplo, el comando siguiente solicita una operación que calcula el valor hash actualizado mediante los archivos encontrados buscando en la ubicación del archivo. manifest actualizado.<br/> <strong>mt.exe-manifest yourComponent. manifest-hashupdate-out: Updated. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>Especifica una operación que realiza una comprobación de sintaxis de la conformidad del manifiesto con el esquema del manifiesto. Por ejemplo, el comando siguiente solicita una comprobación para validar la conformidad de man1. manifest con su esquema. <br/> <strong>mt.exe: manifiesto man1. manifest-validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>Especifica una operación que valida los valores hash de los elementos de <strong>archivo</strong> del manifiesto. Por ejemplo, el comando siguiente solicita una operación que valida los valores hash de todos los elementos de <strong>archivo</strong> de man1. manifest.<br/> <strong>mt.exe-manifest man1. manifest-validate_file_hashes: &quot; c; \files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-canonizar</td>
<td>Especifica una operación para actualizar el manifiesto al formato canónico. Por ejemplo, el comando siguiente actualiza man1. manifest al formato canónico.<br/> <strong>mt.exe: manifiesto man1. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>Especifica una operación que comprueba si hay elementos duplicados en el manifiesto. Por ejemplo, el siguiente comando comprueba man1. manifest en busca de elementos duplicados.<br/> <strong>mt.exe-man1. manifest-check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>Genera archivos. CDF para crear catálogos. Por ejemplo, para el comando siguiente solicita una operación que actualiza el valor hash y genera un archivo. CDF.<br/> <strong>mt.exe-manifest COMP1. manifest-hashupdate-makecdfs-out: Updated. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Muestra información de depuración detallada.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>Cuando se ejecuta con-?, o sin opciones ni argumentos, Mt.exe muestra el texto de ayuda.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de ensamblados en paralelo](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

