---
description: La tabla DrLocator contiene la información necesaria para buscar un archivo o directorio buscando en el árbol de directorios.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Tabla DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1765c7b8f5c38d5701c4c401eb333c7db6a7c403689b8c3100d55b5e51e28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378329"
---
# <a name="drlocator-table"></a>Tabla DrLocator

La tabla DrLocator contiene la información necesaria para buscar un archivo o directorio buscando en el árbol de directorios.

La tabla DrLocator tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificador](identifier.md) | Y   | N        |
| Parent      | [Identificador](identifier.md) | Y   | Y        |
| Ruta de acceso        | [AnyPath](anypath.md)       | Y   | Y        |
| Profundidad       | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

La columna \_ Firma es una clave externa a la primera columna de la tabla [Signature](signature-table.md). Este campo puede representar una firma de archivo única enumerada en la tabla Firma. Si el valor de esta columna no está presente en la tabla Signature, se supone que la búsqueda es para un directorio al que apunta la tabla DrLocator.

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Padre
</dt> <dd>

Esta columna es la firma del directorio primario del archivo o directorio de la columna \_ Firma. Si este campo es NULL y la columna Ruta de acceso no se expande a una ruta de acceso completa, se buscan todas las unidades fijas del sistema del usuario mediante la ruta de acceso.

Este campo es una clave en una de las tablas siguientes: [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)o DrLocator.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Camino
</dt> <dd>

La columna Ruta de acceso contiene la ruta de acceso en el sistema del usuario. Se trata de una ruta de acceso completa o una subpath relativa debajo del directorio especificado en la columna Parent. Consulte las restricciones en el [tipo de datos AnyPath.](anypath.md)

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Profundidad
</dt> <dd>

Profundidad debajo de la ruta de acceso en la que el instalador busca el archivo o directorio especificado en la columna \_ Firma. El valor utilizado en el campo Profundidad se basa en cero. Por ejemplo, si el campo Ruta de acceso es c:/Archivos de programa/bin, la columna Profundidad debe establecerse en 0 o superior para detectar un archivo ubicado dentro del cubo de carpetas. Si el campo Profundidad está vacío, se supone que la profundidad es cero.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).

Por lo general, las columnas de esta tabla no están localizadas. Si un autor decide buscar productos en varios idiomas, debe haber una entrada independiente incluida en la tabla para cada idioma.

Vea [Buscar aplicaciones, archivos, entradas del Registro](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)o entradas de .ini existentes.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



