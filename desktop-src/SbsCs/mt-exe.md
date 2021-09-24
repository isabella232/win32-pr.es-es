---
description: El Mt.exe es una herramienta que genera archivos y catálogos firmados. Está disponible en el Kit de desarrollo Windows software (SDK) de Microsoft. Mt.exe requiere que el archivo al que se hace referencia en el manifiesto esté presente en el mismo directorio que el manifiesto.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8987b4b78a85248eb085b8acf45b1fd364a5da
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521027"
---
# <a name="mtexe"></a>Mt.exe

El Mt.exe es una herramienta que genera archivos y catálogos firmados. Está disponible en el Kit de desarrollo Windows software (SDK) de Microsoft. Mt.exe requiere que el archivo al que se hace referencia en el manifiesto esté presente en el mismo directorio que el manifiesto.

Mt.exe genera hashes mediante la implementación de CryptoAPI del algoritmo hash seguro (SHA-1). Para obtener más información sobre los algoritmos hash, consulte [Algoritmos hash y de firma](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Los hashes se insertan como una cadena hexadecimal en las **etiquetas de** archivo del manifiesto. Actualmente, la herramienta solo genera hash sha-1, aunque los archivos de los manifiestos pueden usar otros esquemas de hash.

Mt.exe usa Makecat.exe para generar archivos de catálogo (.cat) a partir de archivos de definición de catálogo (.cdf). Esta herramienta rellena una cdf de plantilla estándar con el nombre y la ubicación del manifiesto. Puede usarlo con Makecat.exe generar el catálogo de ensamblados.

La versión de Mt.exe proporcionada en versiones recientes del SDK de Windows también se puede usar para generar manifiestos para ensamblados administrados y ensamblados en paralelo no administrados.

## <a name="syntax"></a>Sintaxis

```console
mt.exe [-manifest:<component1.manifest><component2.manifest>] [-identity:<identity string>] 
[-rgs:<file1.rgs>] [-tlb:<file2.tlb>] [-dll:<file3.dll>] [-replacements:<XML filename>]
[-managedassemblyname:<managed assembly>] [-nodependency] [-category] [-out:<output manifest name>]
[-inputresource:<file4>;[#]<resource_id>] [-outputresource:<file5>;[#]<resource_id>] 
[-updateresource:<file6>;[#]<resource_id>] [-hashupdate[:<path to files>]] [-makecdfs] [-validate_manifest]
[-validate_file_hashes:<path to files>] [-canonicalize] [-check_for_duplicates] [-nologo] [-verbose]
```

## <a name="command-line-options"></a>Opciones de la línea de comandos

Mt.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta mayúsculas de minúsculas.



<table>
                    <tr>
                        <th>Opción</th>
                        <th>Descripción</th>
                    </tr>
                    <tr>
                        <td>-manifest</td>
                        <td><p>Especifica el nombre del archivo de manifiesto. Para modificar un único manifiesto, especifique un nombre de archivo de manifiesto.  Por ejemplo, component.manifest.</p> <p>Para combinar varios manifiestos, especifique los nombres de los manifiestos de origen aquí.  Especifique el nombre del manifiesto actualizado con las opciones <i>-out</i>, <i>-outputresource</i>o <i>-updateresource.</i>  Por ejemplo, la siguiente línea de comandos solicita una operación que combina dos manifiestos, man1.manifest y man2.manifest, en un nuevo manifiesto, man3.manifest.</p><p><i>mt.exe -manifest man1.manifest man2.manifest -out:man3.manifest</i></p><p>Sin dos puntos (:) es necesario con la <i>opción -manifest.</i></p></td>
                    </tr>
                    <tr>
                        <td>-identity</td>
                        <td><p>Proporciona los valores de atributos del <strong>elemento assemblyIdentity</strong> del manifiesto. El argumento de la <i>opción -identity</i> es un valor de cadena que contiene los valores de atributo en campos separados por comas.  Proporcione el valor del atributo <strong>name</strong> en el primer campo, sin incluir una subcadena "name=". Todos los campos restantes especifican los atributos y sus valores con el formato: &lt; nombre de atributo attribute_value &gt; = &lt; &gt; .</p><p>Por ejemplo, para actualizar el <strong>elemento assemblyIdentity</strong> del manifiesto con la siguiente información:</p><p>&lt;assemblyIdentity type="win32" name="Microsoft. Windows. SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/&gt; </p><p>incluya la siguiente <i>opción -identity</i> en la línea de comandos:</p><p><i>-identity:</i>"Microsoft. Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5"</p></td>
                    </tr>
                    <tr>
                        <td>-rgs </td>
                        <td><p>Especifica el nombre del archivo de script de registro (.rgs). La <i>opción -dll </i>es necesaria para usar <i>la opción -rgs.</i></p> </td>
                    </tr>
                    <tr>
                        <td>-tlb </td>
                        <td><p>Especifica el nombre del archivo de biblioteca de tipos (.tlb).  La <i>opción -dll </i>es necesaria para usar <i>la opción -tlb.</i></p> </td>
                    </tr>
                    <tr>
                        <td>-dll </td>
                        <td><p>Especifica el nombre del archivo de biblioteca de vínculos dinámicos (DLL). La <i>opción -dll </i>es necesaria <i>mt.exe</i> si se usan las opciones <i>-rgs</i> <i>o -tlb.</i> Especifique el nombre del archivo DLL que va a compilar finalmente a partir de los archivos .rgs o .tlb.</p><p>Por ejemplo, el comando siguiente solicita una operación que genera un manifiesto a partir de archivos .rgs y .tlb.</p><p><i>mt.exe -rgs:testreg1.rgs -tlb:testlib1.tlb -dll:test.dll -replacements:rep.manifest -identity:"Microsoft. Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5" -out:rgstlb.manifest</i> </p> </td>
                    </tr>
                    <tr>
                        <td>-replacements </td>
                        <td><p>Especifica el archivo que contiene los valores de la cadena reemplazable en el archivo .rgs.</p> </td>
                    </tr>
                    <tr>
                        <td>-managedassemblyname </td>
                        <td><p>Genera un manifiesto del ensamblado administrado especificado.  Use con la <i>opción -nodependency</i> para generar un manifiesto sin elementos de dependencia. Use con la <i>opción -category</i> para generar un manifiesto con etiquetas de categoría. Por ejemplo, si managed.dll es un ensamblado administrado, la siguiente línea de comandos genera el archivo out.manifest a partir de managed.dll.</p><p><i>mt.exe -managedassemblyname:managed.dll -out:out.manifest </i></p> </td>
                    </tr>
                    <tr>
                        <td>-nodependency </td>
                        <td><p>Especifica una operación que genera un manifiesto sin elementos de dependencia.  La <i>opción -nodependency</i> requiere la <i>opción -managedassemblyname.</i> Por ejemplo, si managed.dll es un ensamblado administrado, la siguiente línea de comandos genera el archivo out.manifest managed.dll sin información de dependencia.</p><p><i>mt.exe -managedassemblyname:managed.dll -out:out.manifest -nodependency</i></p> </td>
                    </tr>
                    <tr>
                        <td>-category </td>
                        <td><p>Especifica una operación que genera un manifiesto con etiquetas de categoría. La <i>opción -category</i> requiere la <i>opción -managedassemblyname.</i> Por ejemplo, si managed.dll es un ensamblado administrado, la siguiente línea de comandos genera el archivo out.manifest a partir managed.dll etiquetas de categoría.</p><p><i>mt.exe -managedassemblyname:managed.dll -out:out.manifest -category</i></p> </td>
                    </tr>
                    <tr>
                        <td>-nologo</td>
                        <td><p>Especifica una operación que se ejecuta sin mostrar datos estándar de copyright de Microsoft. Si  <i>mt.exe</i> ejecuta como parte de un proceso de compilación, esta opción se puede usar para evitar escribir información no deseada en los archivos de registro. </p></td>
                    </tr>
                    <tr>
                        <td>-out </td>
                        <td><p>Especifica el nombre del manifiesto actualizado.  Si se trata de una operación de un solo manifiesto y se omite <i>la opción -out,</i> se modifica el manifiesto original. </p></td>
                    </tr>
                    <tr>
                        <td>-inputresource </td>
                        <td><p>Especifica una operación realizada en un manifiesto obtenido de un recurso de tipo RT_MANIFEST.  Si se <i>usa la opción -inputresource</i> sin especificar el identificador de recurso, resource_id , la operación usa &lt; el valor &gt; CREATEPROCESS_MANIFEST_RESOURCE. </p><p>Por ejemplo, el comando siguiente solicita una operación que combina un manifiesto de un archivo DLL, dll_with_manifest.dll y un archivo de manifiesto, man2.manifest.  Los manifiestos combinados los recibe un manifiesto en el archivo de recursos de otro archivo DLL, dll_with_merged_manifests. </p><p><i>mt.exe -inputresource:dll_with_manifest.dll;#1 -manifest man2.manifest -outputresource:dll_with_merged_manifest.dll;#3</i></p><p>Para extraer el manifiesto de un archivo DLL, especifique el nombre del archivo DLL.  Por ejemplo, el comando siguiente extrae el manifiesto de lib1.dll y man3.manifest recibe el manifiesto extraído.</p><p><i>mt.exe -inputresource:lib.dll;#1 -out:man3.manifest</i></p></td>
                    </tr>
                    <tr>
                        <td>-outputresource </td>
                        <td><p>Especifica una operación que genera un manifiesto que un recurso de tipo RT_MANIFEST.  Si se <i>usa la opción -outputresource</i> sin especificar el identificador de recurso, resource_id , la operación &lt; usa el valor &gt; CREATEPROCESS_MANIFEST_RESOURCE. </p></td>
                    </tr>
                    <tr>
                        <td>-updateresource </td>
                        <td><p>Especifica una operación equivalente al uso de las opciones <i>-inputresource</i>  y <i>-outputresource</i> con argumentos idénticos. Por ejemplo, el comando siguiente solicita una operación que calcula un hash de los archivos en la ruta de acceso especificada y actualiza el manifiesto de un recurso de un archivo ejecutable portátil (PE).</p><p><i>mt.exe -updateresource:dll_with_manifest.dll;#1 -hashupdate:f:\files</i>.</p> </td>
                    </tr>
                    <tr>
                        <td>-hashupdate </td>
                        <td><p>Calcula el valor hash de los archivos en las rutas de acceso especificadas y actualiza el valor del atributo <strong>hash</strong> del <strong>elemento File</strong> con este valor. </p><p>Por ejemplo, el comando siguiente solicita una operación que combina dos archivos de manifiesto, man1.manifest y man2.manifest, y actualiza el valor del atributo <strong>hash</strong> del elemento <strong>File</strong> del manifiesto que recibe la información combinada, merged.manifest.</p><p><i>mt.exe -manifest man1.manifest man2.manifest -hashupdate:d:\filerepository -out:merged.manifest</i></p><p>Si no se especifican las rutas de acceso a los archivos, la operación busca en la ubicación del manifiesto especificado para recibir la actualización. Por ejemplo, el comando siguiente solicita una operación que calcula el valor hash actualizado mediante los archivos encontrados buscando en la ubicación de updated.manifest.</p><p><i>mt.exe -manifest yourComponent.manifest -hashupdate -out:updated.manifest</i></p></td>
                    </tr>
                    <tr>
                        <td>-validate_manifest </td>
                        <td><p>Especifica una operación que realiza una comprobación de sintaxis de la conformidad del manifiesto con el esquema de manifiesto.  Por ejemplo, el comando siguiente solicita una comprobación para validar la conformidad de man1.manifest con su esquema. </p><p><i>mt.exe -manifest man1.manifest -validate_manifest</i></p> </td>
                    </tr>
                    <tr>
                        <td>-validate_file_hashes </td>
                        <td><p>Especifica una operación que valida los valores hash de los <strong>elementos File</strong> del manifiesto. Por ejemplo, el comando siguiente solicita una operación que valida los valores hash de todos los elementos  <strong>File</strong> del archivo man1.manifest.</p><p><i>mt.exe -manifest man1.manifest -validate_file_hashes:"c;\files"</i></p> </td>
                    </tr>
                    <tr>
                        <td>-canonicalize </td>
                        <td><p>Especifica una operación para actualizar el manifiesto a formato canónico. Por ejemplo, el siguiente comando actualiza man1.manifest a formato canónico.</p><p><i>mt.exe -manifest man1.manifest</i></p> </td>
                    </tr>
                    <tr>
                        <td>-check_for_duplicates </td>
                        <td><p>Especifica una operación que comprueba el manifiesto en busca de elementos duplicados. Por ejemplo, el siguiente comando comprueba si hay elementos duplicados en man1.manifest.</p><p><i>mt.exe -man1.manifest -check_for_duplicates</i></p> </td>
                    </tr>                   
                    <tr>
                        <td>-makecdfs</td>
                        <td><p>Genera archivos .cdf para crear catálogos.  Por ejemplo, al comando siguiente se solicita una operación que actualiza el valor hash y genera un archivo .cdf.</p><p><i>mt.exe -manifest comp1.manifest -hashupdate -makecdfs -out:updated.manifest</i></p></td>
                    </tr>
                    <tr>
                        <td>-verbose</td>
                        <td>Muestra información de depuración detallada. </td>
                    </tr>
                    <tr>
                        <td>-?</td>
                        <td>Cuando se ejecuta -?, sin opciones ni argumentos, Mt.exe texto de ayuda.</td>
                    </tr>
                </table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de ensamblados en paralelo](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

