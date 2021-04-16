---
description: La tabla DrLocator contiene la información necesaria para buscar un archivo o un directorio mediante la búsqueda en el árbol de directorios.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Tabla DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652467"
---
# <a name="drlocator-table"></a>Tabla DrLocator

La tabla DrLocator contiene la información necesaria para buscar un archivo o un directorio mediante la búsqueda en el árbol de directorios.

La tabla DrLocator tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Signatura\_ | [Identificador](identifier.md) | Y   | N        |
| Parent      | [Identificador](identifier.md) | Y   | Y        |
| Ruta        | [AnyPath](anypath.md)       | Y   | Y        |
| Profundidad       | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_
</dt> <dd>

La \_ columna Signature es una clave externa de la primera columna de la [tabla Signature](signature-table.md). Este campo puede representar una firma de archivo única que aparece en la tabla de signatura. Si el valor de esta columna no se encuentra en la tabla de firmas, se supone que la búsqueda es para un directorio al que apunta la tabla DrLocator.

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Aérea
</dt> <dd>

Esta columna es la firma del directorio principal del archivo o directorio en la \_ columna firma. Si este campo es NULL y la columna Path no se expande a una ruta de acceso completa, se busca en todas las unidades fijas del sistema del usuario mediante la ruta de acceso.

Este campo es una clave en una de las tablas siguientes: [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)o DrLocator.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Camino
</dt> <dd>

La columna Path contiene la ruta de acceso en el sistema del usuario. Se trata de una ruta de acceso completa o un subtrazado relativo situado debajo del directorio especificado en la columna primaria. Vea las restricciones en el tipo de datos [AnyPath](anypath.md) .

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Amplia
</dt> <dd>

La profundidad por debajo de la ruta de acceso en la que el instalador busca el archivo o directorio especificado en la columna de firma \_ . El valor usado en el campo de profundidad se basa en cero. Por ejemplo, si el campo de ruta de acceso es c:/archivos de programa/bin, la columna de profundidad debe establecerse en 0 o más para detectar un archivo ubicado dentro de la ubicación de la carpeta. Si el campo de profundidad está vacío, se supone que la profundidad es cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).

Por lo general, las columnas de esta tabla no están localizadas. Si un autor decide buscar productos en varios idiomas, debe haber una entrada independiente incluida en la tabla para cada idioma.

Vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



