---
description: La tabla de archivos contiene una lista completa de archivos de origen con sus distintos atributos, ordenados por un identificador único no localizado.
ms.assetid: 31d0e727-a9eb-4cd2-a211-ea7b138d0173
title: Tabla de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59838001101bbc65af50bff3f2b00b540976e4b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074797"
---
# <a name="file-table"></a>Tabla de archivos

La tabla de archivos contiene una lista completa de archivos de origen con sus distintos atributos, ordenados por un identificador único no localizado. Los archivos se pueden almacenar en el medio de origen como archivos individuales o comprimirse dentro de un [*archivo de archivador*](c-gly.md). Para obtener más información, [vea Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

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

<span id="File"></span><span id="file"></span><span id="FILE"></span>Archivo
</dt> <dd>

Token no localizado que identifica de forma única el archivo. Este campo no tiene en cuenta las mayúsculas y minúsculas. No asigne identificadores a archivos diferentes que solo difieren en su caso.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la [tabla de componentes](component-table.md). Este campo identifica el componente que controla el archivo.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nombre
</dt> <dd>

Nombre de archivo usado para la instalación. El nombre se puede localizar.

Dado que algunos servidores web pueden distingue mayúsculas de minúsculas, FileName debe coincidir exactamente con el caso de los archivos de origen para garantizar la compatibilidad con las descargas de Internet.

</dd> <dt>

<span id="FileSize"></span><span id="filesize"></span><span id="FILESIZE"></span>Tamaño
</dt> <dd>

El tamaño del archivo en bytes. Debe ser un número no negativo.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versión
</dt> <dd>

Este campo es la cadena de versión de un archivo con versión. Este campo está en blanco para los archivos sin control de versiones. La versión del archivo especificada en este campo debe ser idéntica a la versión del archivo incluido con el paquete de instalación.

El campo Versión también se puede establecer para que contenga la clave principal de otro registro en la tabla Archivo. A continuación, el archivo al que se hace referencia determina la lógica de control de versiones para este archivo. Para obtener más información, vea [Archivos complementarios](companion-files.md). Tenga en cuenta que si este archivo es la ruta de acceso de clave para su componente, no debe especificarse como un archivo complementario.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Lengua
</dt> <dd>

Lista de los IDs de idioma decimal separados por comas.

Los archivos de fuente no deben crearse con un identificador de idioma, ya que las fuentes no tienen un recurso de identificador de idioma incrustado. Por lo tanto, esta columna debe dejársela como NULL para los archivos de fuente.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Entero que contiene marcas de bits que representan atributos de archivo.

En la tabla siguiente se muestra la definición del campo de bits.



| Constante                             | Hexadecimal | Decimal | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbFileAttributesReadOnly**      | 0x000001    | 1       | Solo lectura                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **msidbFileAttributesHidden**        | 0x000002    | 2       | Hidden                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesSystem**        | 0x000004    | 4       | Sistema                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesVital**         | 0x000200    | 512     | El archivo es fundamental para el funcionamiento preciso del componente al que pertenece. Si se produce un error en la instalación de un archivo con el atributo msidbFileAttributesVital, la instalación se detiene y se revierte. En este caso, el instalador muestra un cuadro de diálogo sin un botón Omitir. Si no se establece este atributo y se produce un error en la instalación del archivo, el instalador muestra un cuadro de diálogo con un botón Omitir. En este caso, el usuario puede optar por omitir el error al instalar el archivo y continuar. <br/> |
| **msidbFileAttributesChecksum**      | 0x000400    | 1024    | El archivo contiene una suma de [*comprobación válida.*](c-gly.md) Se requiere una suma de comprobación para reparar un archivo que se ha dañado.                                                                                                                                                                                                                                                                                                                                                                                           |
| **msidbFileAttributesPatchAdded**    | 0x001000    | 4096    | Este bit solo debe agregarse mediante una revisión y si la revisión agrega el archivo.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **msidbFileAttributesNoncompressed** | 0x002000    | 8192    | El tipo de origen del archivo no está comprimido. Si se establece, ignore la [**propiedad Resumen de recuento de**](word-count-summary.md) palabras. Si no **se establecen msidbFileAttributesNoncompressed** o **msidbFileAttributesCompressed,** la propiedad **Resumen** de recuento de palabras especifica el estado de compresión del archivo. No establezca **msidbFileAttributesNoncompressed y** **msidbFileAttributesCompressed.**                                                                                                                            |
| **msidbFileAttributesCompressed**    | 0x004000    | 16384   | El tipo de origen del archivo está comprimido. Si se establece, ignore la [**propiedad Resumen de recuento de**](word-count-summary.md) palabras. Si no **se establecen msidbFileAttributesNoncompressed** o **msidbFileAttributesCompressed,** la propiedad **Resumen** de recuento de palabras especifica el estado de compresión del archivo. No establezca **msidbFileAttributesNoncompressed y** **msidbFileAttributesCompressed.**                                                                                                                              |



 

Si se establece el bit **msidbFileAttributesVital** dentro de la columna Atributos y si el componente al que pertenece el archivo está seleccionado para la instalación, el instalador debe poder instalar este archivo para que la instalación se complete correctamente. Si el instalador no puede instalar el archivo por algún motivo (por ejemplo, si el archivo de origen no se puede encontrar dentro de la imagen de origen), aparecerá un cuadro de diálogo de error con las opciones "Reintentar" o "Cancelar". Para un archivo que no tiene **msidbFileAttributesVital** establecido, las opciones en caso de error de instalación serán "Abort", "Retry" e "Ignore" (es decir, el usuario tendrá la opción de completar la instalación correctamente sin instalar ese archivo).

El bit **msidbFileAttributesChecksum** de la columna Atributos debe establecerse para [](c-gly.md) cada archivo ejecutable de la instalación que tenga una suma de comprobación válida almacenada en el encabezado de archivo Portable Executable (PE). Solo los archivos que tienen este conjunto de bits se comprobarán alguna vez para la suma de comprobación válida durante una reinstalación. Para obtener más información, vea [**REINSTALLMODE**](reinstallmode.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

Posición de secuencia de este archivo en las imágenes multimedia. Este orden debe corresponder al orden de los archivos del archivador si los archivos están comprimidos. Los enteros de este campo deben ser iguales o mayores que 1.

Los números de secuencia de la columna Secuencia se usan para especificar el orden de instalación de los archivos y los medios de origen en los que se encuentra el archivo (junto con la [tabla multimedia](media-table.md)). Por ejemplo, suponga que un archivo tiene un número de secuencia de 92. Para determinar el disco de origen en el que reside este archivo, busque en la tabla Media la entrada con el valor más pequeño de Last Sequence mayor que 92.

Aunque a los archivos comprimidos se les asignan números de secuencia internos dentro de los gabinetes, esos números absolutos no necesitan coincidir con los números de secuencia de la tabla Archivo. Sin embargo, es importante que la secuencia de archivos de la tabla File sea idéntica a la secuencia de los archivos dentro de los archivadores.

Para los archivos que no están comprimidos, los números de secuencia no deben ser únicos. Por ejemplo, si todos los archivos están descomprimidos y todos residen en un disco, podría dar a todos los archivos el mismo número de secuencia.

El límite máximo es de 32767 archivos. Para crear un paquete Windows Installer con más archivos, vea [Creación de un paquete grande.](authoring-a-large-package.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las [acciones InstallFiles](installfiles-action.md) [y RemoveFiles](removefiles-action.md) de las tablas [*de secuencia*](s-gly.md) procesan la información de esta tabla. Para obtener información sobre el *uso de tablas de secuencia,* vea Usar una tabla de [secuencia.](using-a-sequence-table.md)

La tabla se genera inicialmente a partir de la lista de archivos, pero si se usa la compresión de gabinete, la tabla se vuelve a generar a partir de la salida del motor de compresión. Para obtener más información, vea [Archivos archivadores](cabinet-files.md).

Para mover un archivo existente en el equipo del usuario durante la instalación, use la acción [MoveFiles](movefiles-action.md) y la [tabla MoveFile](movefile-table.md). Para instalar un archivo en varias ubicaciones, use [la acción DuplicateFiles](duplicatefiles-action.md) y [la tabla DuplicateFile](duplicatefile-table.md).

En la tabla siguiente se resumen las posibles combinaciones de valores de la columna Versión y la columna Idioma. Para obtener más información, vea [Reglas de control de versiones de archivos](file-versioning-rules.md).



| Versión | Idioma | Descripción                                                                     |
|---------|----------|---------------------------------------------------------------------------------|
| 1.2.3.4 | 3082     | Versión e idioma.                                                       |
| 1.2.3.4 | (Null)   | Versión pero sin idioma.                                                    |
| 1.2.3.4 | 0        | La versión y el idioma son neutros.                                           |
| Testdb  | (Null)   | Archivo complementario sin idioma asociado a él.                         |
| Testdb  | 3082     | El archivo complementario y el idioma.                                                |
| (Null)  | 3082     | No hay ninguna versión, pero tiene un lenguaje asociado (es decir, typelib, helpfile). |



 

Para obtener más información, [vea MsiLockPermissionsEx Table](msilockpermissionsex-table.md) y [LockPermissions Table](lockpermissions-table.md).

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

 

 




