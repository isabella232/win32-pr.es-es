---
description: La tabla AppSearch contiene las propiedades necesarias para buscar un archivo que tenga una firma de archivo determinada. La tabla AppSearch también se puede usar para establecer una propiedad en el valor existente de una entrada del archivo Registry o. ini.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Tabla AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276523"
---
# <a name="appsearch-table"></a>Tabla AppSearch

La tabla AppSearch contiene las propiedades necesarias para buscar un archivo que tenga una firma de archivo determinada. La tabla AppSearch también se puede usar para establecer una propiedad en el valor existente de una entrada del archivo Registry o. ini.

La tabla AppSearch tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Propiedad    | [Identificador](identifier.md) | Y   | N        |
| Signatura\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Al ejecutar la acción [AppSearch](appsearch-action.md) se establece esta propiedad en la ubicación del archivo indicado por la \_ columna Signature. Esta propiedad se establece si la firma de archivo existe en el equipo del usuario. Las propiedades utilizadas en esta columna deben ser propiedades [públicas](public-properties.md) y tener un identificador que no contenga ninguna letra minúscula.

La propiedad enumerada en el campo de propiedad se puede inicializar en la tabla de [propiedades](property-table.md) o desde una línea de comandos. Si la acción [AppSearch](appsearch-action.md) localiza la firma, el instalador invalida el valor de la propiedad inicializado con el valor encontrado. Si no se encuentra la firma, se utiliza el valor de la propiedad inicial. Si nunca se inicializó la propiedad, la propiedad solo se establecerá si se encuentra la firma. De lo contrario, la propiedad no está definida.

</dd> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatura\_
</dt> <dd>

La \_ columna Signature contiene un identificador único denominado Signature y también es una clave externa en las tablas [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)y [DrLocator](drlocator-table.md) . Al buscar un archivo, el valor de esta columna también debe ser una clave externa en la tabla de [signatura](signature-table.md) . Si el valor de esta columna no aparece en la tabla de firmas, el instalador determina que la búsqueda es para un directorio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La acción [AppSearch](appsearch-action.md) de [*las tablas de secuencia*](s-gly.md) procesa la información de esta tabla. Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).

La acción [AppSearch](appsearch-action.md) busca firmas mediante la tabla [CompLocator](complocator-table.md) en primer lugar, la tabla [RegLocator](reglocator-table.md) Second, la tabla [IniLocator](inilocator-table.md) Third y, por último, la tabla [DrLocator](drlocator-table.md) . Las firmas de archivo se muestran en la tabla de [firmas](signature-table.md) . Una firma que no está en la tabla de signatura denota un directorio y la acción establece la propiedad en la ruta de acceso del directorio para esa firma.

Vea [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE52](ice52.md)  
[ICE88](ice88.md)  
</dl>

 

 



