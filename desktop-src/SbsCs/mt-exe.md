---
description: El Mt.exe es una herramienta que genera archivos y catálogos firmados. Está disponible en Microsoft Windows Software Development Kit (SDK). Mt.exe requiere que el archivo al que se hace referencia en el manifiesto esté presente en el mismo directorio que el manifiesto.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb81f3e0b7bf6b67236f1bd6037d1eceb11e0b89
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623912"
---
# <a name="mtexe"></a>Mt.exe

El Mt.exe es una herramienta que genera archivos y catálogos firmados. Está disponible en Microsoft Windows Software Development Kit (SDK). Mt.exe requiere que el archivo al que se hace referencia en el manifiesto esté presente en el mismo directorio que el manifiesto.

Mt.exe genera hashes mediante la implementación cryptoAPI del algoritmo hash seguro (SHA-1). Para obtener más información sobre los algoritmos hash, consulte [Algoritmos hash y de firma](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Los hashes se insertan como una cadena hexadecimal en las **etiquetas de** archivo del manifiesto. Actualmente, la herramienta solo genera hash SHA-1, aunque los archivos de los manifiestos pueden usar otros esquemas de hash.

Mt.exe usa Makecat.exe para generar archivos de catálogo (.cat) a partir de archivos de definición de catálogo (.cdf). Esta herramienta rellena una plantilla estándar de CDF con el nombre y la ubicación del manifiesto. Puede usarlo con Makecat.exe generar el catálogo de ensamblados.

La versión de Mt.exe proporcionada en versiones recientes del SDK de Windows también se puede usar para generar manifiestos para ensamblados administrados y ensamblados no administrados en paralelo.

## <a name="syntax"></a>Sintaxis

**mt.exe \[ -manifest** _<component1.manifest><component2.manifest>_ *_\] \[ -identity:_* *<identity string> * **\] \[ -rgs:**<_file1.rgs>_* _\] \[ -tlb:_<*_file2.tlb>_* _\] \[ -dll:_ *_<file3.dll>_* _\] \[ -replacements:_ *_<XML filename>_* _\] \[ -managedassemblyname:_ *_<managed assembly>_* _\] \[ -nodependency \] \[ -category \] \[ -out:_ *_<output manifest name>_* _\] \[ -inputresource:_ *_<file4>_* _; \[ \# \]_ *_><0 \_ id. de recurso><1_* _\] \[ -outputresource:_ *_<file5>_* _; \[ \# \]_ *_><2 \_ id. de recurso><3_* _\] \[ -updateresource:_ *_<file6>_* _; \[ \# \]_><4 id. *_\_ de recurso><5_* _\] \[ -hashupdate \[ :_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -validate \_ manifest \] \[ -validate file \_ \_ hashes:_ *_<path to files>_* _\] \[ -canonicalize \] \[ -check \_ for \_ duplicates \] \[ -nologo \] \[ -verbose \]_*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Mt.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas.



<table>
<colgroup>
<col  />
<col  />
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
<td>Especifica el nombre del archivo de manifiesto. Para modificar un único manifiesto, especifique un nombre de archivo de manifiesto. Por ejemplo, component.manifest.<br/> Para combinar varios manifiestos, especifique los nombres de los manifiestos de origen aquí. Especifique el nombre del manifiesto actualizado con las opciones <strong>-out</strong>, <strong>-outputresource</strong>o <strong>-updateresource.</strong> Por ejemplo, la siguiente línea de comandos solicita una operación que combina dos manifiestos, man1.manifest y man2.manifest, en un nuevo manifiesto, man3.manifest.<br/> <strong>mt.exe -manifest man1.manifest man2.manifest -out:man3.manifest</strong><br/>
<blockquote>
[!Note]<br />
Sin dos puntos (:) se requiere con la <strong>opción -manifest.</strong>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-identity</td>
<td>Proporciona los valores de atributos del <strong>elemento assemblyIdentity</strong> del manifiesto. El argumento de la <strong>opción -identity</strong> es un valor de cadena que contiene los valores de atributo en campos separados por comas. Proporcione el valor del atributo <strong>name</strong> en el primer campo, sin incluir una &quot; &quot; subcadena name=. Todos los campos restantes especifican los atributos y sus valores con el formato : <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Por ejemplo, para actualizar el <strong>elemento assemblyIdentity</strong> del manifiesto con la siguiente información:<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> incluya la siguiente <strong>opción -identity</strong> en la línea de comandos:<br/> <strong>-identity:</strong> &quot; Microsoft. Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-rgs</td>
<td>Especifica el nombre del archivo de script de registro (.rgs). La <strong>opción -dll</strong> es necesaria para usar <strong>la opción -rgs.</strong><br/></td>
</tr>
<tr class="even">
<td>-tlb</td>
<td>Especifica el nombre del archivo de biblioteca de tipos (.tlb). La <strong>opción -dll</strong> es necesaria para usar <strong>la opción -tlb.</strong><br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>Especifica el nombre del archivo de biblioteca de vínculos dinámicos (DLL). La <strong>opción -dll</strong> es necesaria <strong>mt.exe</strong> si se usan las opciones <strong>-rgs</strong> <strong>o -tlb.</strong> Especifique el nombre del archivo DLL que piensa compilar a partir de los archivos .rgs o .tlb.<br/> Por ejemplo, el comando siguiente solicita una operación que genera un manifiesto a partir de archivos .rgs y .tlb.<br/> <strong>mt.exe -rgs:testreg1.rgs -tlb:testlib1.tlb -dll:test.dll -replacements:rep.manifest -identity: &quot; Microsoft.Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5 &quot; -out:rgstlb.manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-replacements</td>
<td>Especifica el archivo que contiene los valores de la cadena reemplazable en el archivo .rgs.<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>Genera un manifiesto del ensamblado administrado especificado. Use con la <strong>opción -nodependency para</strong> generar un manifiesto sin elementos de dependencia. Use con la <strong>opción -category</strong> para generar un manifiesto con etiquetas de categoría. Por ejemplo, si managed.dll es un ensamblado administrado, la siguiente línea de comandos genera el archivo out.manifest a partir managed.dll.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-nodependency</td>
<td>Especifica una operación que genera un manifiesto sin elementos de dependencia. La <strong>opción -nodependency</strong> requiere la <strong>opción -managedassemblyname.</strong> Por ejemplo, si managed.dll es un ensamblado administrado, la siguiente línea de comandos genera el archivo out.manifest managed.dll sin información de dependencia.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest -nodependency</strong><br/></td>
</tr>
<tr class="odd">
<td>-category</td>
<td>Especifica una operación que genera un manifiesto con etiquetas de categoría. La <strong>opción -category</strong> requiere la <strong>opción -managedassemblyname.</strong> Por ejemplo, si managed.dll es un ensamblado administrado, la siguiente línea de comandos genera el archivo out.manifest managed.dll etiquetas de categoría.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest -category</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Especifica una operación que se ejecuta sin mostrar datos estándar de copyright de Microsoft. Si <strong>mt.exe</strong> ejecuta como parte de un proceso de compilación, esta opción se puede usar para evitar escribir información no deseada en los archivos de registro. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Especifica el nombre del manifiesto actualizado. Si se trata de una operación de un solo manifiesto y se omite la opción <strong>-out,</strong> se modifica el manifiesto original. <br/></td>
</tr>
<tr class="even">
<td>-inputresource</td>
<td>Especifica una operación realizada en un manifiesto obtenido de un recurso de tipo RT_MANIFEST. Si se <strong>usa la opción -inputresource</strong> sin especificar el identificador de recurso, , la operación <em> <resource_id> </em> usa el valor CREATEPROCESS_MANIFEST_RESOURCE. <br/> Por ejemplo, el comando siguiente solicita una operación que combina un manifiesto de un archivo DLL, dll_with_manifest.dll y un archivo de manifiesto, man2.manifest. Los manifiestos combinados los recibe un manifiesto en el archivo de recursos de otro archivo DLL, dll_with_merged_manifests. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll;#1 -manifest man2.manifest -outputresource:dll_with_merged_manifest.dll;#3</strong><br/> Para extraer el manifiesto de un archivo DLL, especifique el nombre del archivo DLL. Por ejemplo, el siguiente comando extrae el manifiesto de lib1.dll y man3.manifest recibe el manifiesto extraído.<br/> <strong>mt.exe -inputresource:lib.dll;#1 -out:man3.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>Especifica una operación que genera un manifiesto que un recurso de tipo RT_MANIFEST. Si se <strong>usa la opción -outputresource</strong> sin especificar el identificador de recurso, , la <em> <resource_id> </em> operación usa el valor CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-updateresource</td>
<td>Especifica una operación equivalente al uso de las opciones <strong>-inputresource</strong> y <strong>-outputresource</strong> con argumentos idénticos. Por ejemplo, el comando siguiente solicita una operación que calcula un hash de los archivos en la ruta de acceso especificada y actualiza el manifiesto de un recurso de un ejecutable portable (PE).<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll;#1 -hashupdate:f:\files</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>Calcula el valor hash de los archivos en las rutas de acceso especificadas y actualiza el valor del atributo <strong>hash</strong> del <strong>elemento File</strong> con este valor. <br/> Por ejemplo, el comando siguiente solicita una operación que combina dos archivos de manifiesto, man1.manifest y man2.manifest, y actualiza el valor del atributo <strong>hash</strong> del elemento <strong>File</strong> del manifiesto que recibe la información combinada, merged.manifest.<br/> <strong>mt.exe -manifest man1.manifest man2.manifest -hashupdate:d:\filerepository -out:merged.manifest</strong><br/> Si no se especifican las rutas de acceso a los archivos, la operación busca en la ubicación del manifiesto especificado para recibir la actualización. Por ejemplo, el comando siguiente solicita una operación que calcula el valor hash actualizado mediante los archivos encontrados buscando en la ubicación de updated.manifest.<br/> <strong>mt.exe -manifest yourComponent.manifest -hashupdate -out:updated.manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>Especifica una operación que realiza una comprobación de sintaxis de la conformidad del manifiesto con el esquema de manifiesto. Por ejemplo, el comando siguiente solicita una comprobación para validar la conformidad de man1.manifest con su esquema. <br/> <strong>mt.exe -manifest man1.manifest -validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>Especifica una operación que valida los valores hash de los <strong>elementos File</strong> del manifiesto. Por ejemplo, el comando siguiente solicita una operación que valida los valores hash de todos los elementos <strong>File</strong> del archivo man1.manifest.<br/> <strong>mt.exe -manifest man1.manifest -validate_file_hashes: &quot; c;\files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-canonicalize</td>
<td>Especifica una operación para actualizar el manifiesto al formato canónico. Por ejemplo, el comando siguiente actualiza man1.manifest a un formato canónico.<br/> <strong>mt.exe -manifest man1.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>Especifica una operación que comprueba el manifiesto en busca de elementos duplicados. Por ejemplo, el siguiente comando comprueba si hay elementos duplicados en man1.manifest.<br/> <strong>mt.exe -man1.manifest -check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>Genera archivos .cdf para crear catálogos. Por ejemplo, al comando siguiente se solicita una operación que actualiza el valor hash y genera un archivo .cdf.<br/> <strong>mt.exe -manifest comp1.manifest -hashupdate -makecdfs -out:updated.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Muestra información detallada de depuración.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>Cuando se ejecuta -?, sin opciones ni argumentos, Mt.exe texto de ayuda.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de ensamblados en paralelo](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

