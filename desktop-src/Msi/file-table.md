---
description: La tabla de archivos contiene una lista completa de los archivos de origen con sus distintos atributos, ordenados por un identificador único no localizado.
ms.assetid: 31d0e727-a9eb-4cd2-a211-ea7b138d0173
title: Tabla de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59838001101bbc65af50bff3f2b00b540976e4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911661"
---
# <a name="file-table"></a>Tabla de archivos

La tabla de archivos contiene una lista completa de los archivos de origen con sus distintos atributos, ordenados por un identificador único no localizado. Los archivos se pueden almacenar en el medio de origen como archivos individuales o comprimirse dentro de un [*archivo. cab*](c-gly.md). Para obtener más información, consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).

La tabla de archivos tiene las columnas siguientes.



| Columna      | Tipo                               | Clave | Nullable |
|-------------|------------------------------------|-----|----------|
| Archivo        | [Identificador](identifier.md)       | Y   | N        |
| Componente\_ | [Identificador](identifier.md)       | N   | N        |
| FileName    | [Nombre de archivo](filename.md)           | N   | N        |
| FileSize    | [DoubleInteger](doubleinteger.md) | N   | N        |
| Versión     | [Versión](version.md)             | N   | Y        |
| Idioma    | [Lenguaje](language.md)           | N   | Y        |
| Atributos  | [Entero](integer.md)             | N   | Y        |
| Secuencia    | [Entero](integer.md)             | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>Filesystem
</dt> <dd>

Un token no traducido que identifica de forma única el archivo. Este campo no distingue entre mayúsculas y minúsculas. No asigne identificadores a archivos diferentes que solo difieran en su caso.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

La clave externa en la primera columna de la [tabla de componentes](component-table.md). Este campo identifica el componente que controla el archivo.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión
</dt> <dd>

Nombre de archivo que se usa para la instalación. El nombre se puede localizar.

Dado que algunos servidores Web pueden distinguir mayúsculas de minúsculas, FileName debe coincidir exactamente con las mayúsculas y minúsculas de los archivos de origen para garantizar la compatibilidad con las descargas de Internet.

</dd> <dt>

<span id="FileSize"></span><span id="filesize"></span><span id="FILESIZE"></span>FileSize
</dt> <dd>

El tamaño del archivo en bytes. Debe ser un número no negativo.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versión
</dt> <dd>

Este campo es la cadena de versión de un archivo con versiones. Este campo está en blanco para los archivos sin versión. La versión del archivo especificada en este campo debe ser idéntica a la versión del archivo incluido con el paquete de instalación.

El campo version también puede configurarse para que contenga la clave principal de otro registro en la tabla File. A continuación, el archivo al que se hace referencia determina la lógica de control de versiones para este archivo. Para obtener más información, consulte [Companion files](companion-files.md). Tenga en cuenta que si este archivo es la ruta de acceso de la clave de su componente, no debe especificarse como un archivo complementario.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Módulo
</dt> <dd>

Lista de identificadores de idiomas decimales separados por comas.

Los archivos de fuentes no deben crearse con un identificador de idioma, ya que las fuentes no tienen un recurso de identificador de idioma incrustado. Por lo tanto, esta columna debe dejarse como null para los archivos de fuentes.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

Entero que contiene marcadores de bits que representan atributos de archivo.

En la tabla siguiente se muestra la definición del campo de bits.



| Constante                             | Hexadecimal | Decimal | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbFileAttributesReadOnly**      | 0x000001    | 1       | Solo lectura                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **msidbFileAttributesHidden**        | 0x000002    | 2       | Hidden                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesSystem**        | 0x000004    | 4       | Sistema                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesVital**         | 0x000200    | 512     | El archivo es fundamental para el funcionamiento preciso del componente al que pertenece. Si se produce un error en la instalación de un archivo con el atributo msidbFileAttributesVital, la instalación se detiene y se revierte. En este caso, el instalador muestra un cuadro de diálogo sin un botón Omitir. Si no se establece este atributo y se produce un error en la instalación del archivo, el instalador muestra un cuadro de diálogo con un botón Omitir. En este caso, el usuario puede optar por omitir el error para instalar el archivo y continuar. <br/> |
| **msidbFileAttributesChecksum**      | 0x000400    | 1024    | El archivo contiene una [*suma de comprobación*](c-gly.md)válida. Se requiere una suma de comprobación para reparar un archivo que ha resultado dañado.                                                                                                                                                                                                                                                                                                                                                                                           |
| **msidbFileAttributesPatchAdded**    | 0x001000    | 4096    | Este bit solo debe agregarse mediante una revisión y si la revisión agrega el archivo.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **msidbFileAttributesNoncompressed** | 0x002000    | 8192    | El tipo de origen del archivo no está comprimido. Si se establece, se omite la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) . Si no se establece **msidbFileAttributesNoncompressed** ni **msidbFileAttributesCompressed** , el estado de compresión del archivo se especifica mediante la propiedad de **Resumen de recuento de palabras** . No establezca **msidbFileAttributesNoncompressed** y **msidbFileAttributesCompressed**.                                                                                                                            |
| **msidbFileAttributesCompressed**    | 0x004000    | 16384   | El tipo de origen del archivo está comprimido. Si se establece, se omite la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) . Si no se establece **msidbFileAttributesNoncompressed** ni **msidbFileAttributesCompressed** , el estado de compresión del archivo se especifica mediante la propiedad de **Resumen de recuento de palabras** . No establezca **msidbFileAttributesNoncompressed** y **msidbFileAttributesCompressed**.                                                                                                                              |



 

Si se establece el bit **msidbFileAttributesVital** en la columna atributos y se selecciona el componente al que pertenece el archivo para su instalación, el instalador debe ser capaz de instalar este archivo para que la instalación se complete correctamente. Si el instalador no puede instalar el archivo por algún motivo (por ejemplo, si el archivo de origen no se encuentra dentro de la imagen de origen), aparecerá un cuadro de diálogo de error con las opciones "Reintentar" o "Cancelar". Para un archivo que no tiene **msidbFileAttributesVital** establecido, las opciones en caso de error de instalación serán "Abort", "Retry" y "ignore" (es decir, el usuario tendrá la opción de completar la instalación correctamente sin instalar el archivo).

El bit **msidbFileAttributesChecksum** dentro de la columna Attributes debe establecerse para cada archivo ejecutable de la instalación que tenga una [*suma de comprobación*](c-gly.md) válida almacenada en el encabezado del archivo portable ejecutable (PE). Solo se comprobará la suma de comprobación válida durante una reinstalación de los archivos que tengan este bit establecido. Para obtener más información, vea el [**REINSTALLMODE**](reinstallmode.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ
</dt> <dd>

Posición de la secuencia de este archivo en las imágenes multimedia. Este orden debe corresponder al orden de los archivos en el archivo. cab si los archivos están comprimidos. Los enteros de este campo deben ser iguales o mayores que 1.

Los números de secuencia de la columna secuencia se utilizan para especificar el orden de instalación de los archivos y el medio de origen en el que se encuentra el archivo (junto con la [tabla de medios](media-table.md)). Por ejemplo, supongamos que un archivo tiene un número de secuencia de 92. Para determinar el disco de origen en el que reside este archivo, busque en la tabla de medios la entrada con el menor valor de la última secuencia mayor que 92.

Aunque los archivos comprimidos tienen asignados números de secuencia internos dentro de los contenedores, no es necesario que coincidan con los números de secuencia de la tabla de archivos. Sin embargo, es importante que la secuencia de archivos de la tabla de archivos sea idéntica a la secuencia de los archivos dentro de los contenedores.

En el caso de los archivos que no estén comprimidos, los números de secuencia no deben ser únicos. Por ejemplo, si todos los archivos están sin comprimir y todos residen en un disco, puede asignar a todos los archivos el mismo número de secuencia.

El límite máximo es de 32767 archivos. Para crear un paquete de Windows Installer con más archivos, consulte [crear un paquete de gran tamaño](authoring-a-large-package.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las acciones [InstallFiles](installfiles-action.md) y [RemoveFiles](removefiles-action.md) de las [*tablas de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

La tabla se genera inicialmente a partir de la lista de archivos, pero si se usa la compresión del archivo. la tabla se regenera a partir de la salida del motor de compresión. Para obtener más información, consulte [archivos. cab](cabinet-files.md).

Para trasladar un archivo existente en el equipo del usuario durante la instalación, use la [acción MoveFiles](movefiles-action.md) y la [tabla MoveFile](movefile-table.md). Para instalar un archivo en varias ubicaciones, use la [acción DuplicateFiles](duplicatefiles-action.md) y la [tabla DuplicateFile](duplicatefile-table.md).

En la tabla siguiente se resumen las posibles combinaciones de valores de la columna versión y la columna idioma. Para obtener más información, vea [reglas de control de versiones de archivos](file-versioning-rules.md).



| Versión | Idioma | Descripción                                                                     |
|---------|----------|---------------------------------------------------------------------------------|
| 1.2.3.4 | 3082     | La versión y el idioma.                                                       |
| 1.2.3.4 | Acepta   | La versión pero no el idioma.                                                    |
| 1.2.3.4 | 0        | La versión y el idioma son neutros.                                           |
| TestDB  | Acepta   | Archivo complementario sin idioma asociado.                         |
| TestDB  | 3082     | El archivo complementario y el idioma.                                                |
| Acepta  | 3082     | Sin versión, pero tiene un lenguaje asociado (es decir, typelib, HelpFile). |



 

Para obtener más información, vea la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) y la [tabla LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE39](ice39.md)  
[ICE42](ice42.md)  
[ICE45](ice45.md)  
[ICE50](ice50.md)  
[ICE51](ice51.md)  
[ICE54](ice54.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE60](ice60.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE76](ice76.md)  
[ICE91](ice91.md)  
</dl>

 

 




