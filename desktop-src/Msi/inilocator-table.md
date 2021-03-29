---
description: La tabla IniLocator contiene la información necesaria para buscar un archivo o directorio mediante un archivo. ini o para buscar una entrada. ini determinada. El archivo. ini debe estar presente en el directorio predeterminado de Microsoft Windows.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Tabla IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652571"
---
# <a name="inilocator-table"></a>Tabla IniLocator

La tabla IniLocator contiene la información necesaria para buscar un archivo o directorio mediante un archivo. ini o para buscar una entrada. ini determinada. El archivo. ini debe estar presente en el directorio predeterminado de Microsoft Windows.

La tabla IniLocator tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Signatura\_ | [Identificador](identifier.md) | Y   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| Sección     | [Texto](text.md)             | N   | N        |
| Clave         | [Texto](text.md)             | N   | N        |
| Campo       | [Entero](integer.md)       | N   | Y        |
| Tipo        | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_
</dt> <dd>

Una clave externa en la primera columna de la [tabla de firma](signature-table.md). La firma \_ representa una firma única y también es la clave externa en la columna uno de la tabla de signatura. Si esta firma está presente en la tabla de firmas, la búsqueda es para un archivo. Si esta clave no está presente en la tabla de firmas y el valor de la columna Type es **msidbLocatorTypeRawValue**, la búsqueda es para la entrada. ini especificada por la tabla IniLocator. En caso contrario, la búsqueda es para un directorio especificado por la tabla IniLocator.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extensión
</dt> <dd>

Nombre del archivo. ini.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Transversal
</dt> <dd>

Nombre de sección dentro del archivo. ini.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Clave
</dt> <dd>

Valor de clave dentro de la sección.

</dd> <dt>

<span id="Field"></span><span id="field"></span><span id="FIELD"></span>Campo
</dt> <dd>

Campo de la línea. ini. Si el campo es null o 0, se leerá toda la línea. Debe ser un número no negativo.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente
</dt> <dd>

Un valor que determina si el valor de. ini es una ubicación de archivo, una ubicación de directorio o un valor de. ini sin formato.

En la tabla siguiente se enumeran los valores válidos. Si no está presente, el tipo se establece en 1.



| Constante                      | Hexadecimal | Decimal | Descripción           |
|-------------------------------|-------------|---------|-----------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Ubicación del directorio. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Ubicación del archivo.      |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | Un valor de. ini sin formato.     |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla se usa con la [tabla AppSearch](appsearch-table.md).

Por lo general, las columnas de esta tabla no están localizadas. Si un autor decide buscar productos en varios idiomas, puede haber una entrada independiente incluida en la tabla para cada idioma.

El texto localizado asociado para la presentación o el registro de progreso se especifica en la [tabla ActionText](actiontext-table.md).

Vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



