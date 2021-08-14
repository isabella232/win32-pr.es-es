---
description: La tabla ModuleExclusion mantiene una lista de otros módulos de combinación incompatibles en la misma base de datos del instalador.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: ModuleExclusion Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 008d10e65d81b5668821e1a999cf08f5a10c55db3372a4b0230d560462a977c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996445"
---
# <a name="moduleexclusion-table"></a>ModuleExclusion Table

La tabla ModuleExclusion mantiene una lista de otros módulos de combinación incompatibles en la misma base de datos del instalador. Esta tabla permite que una herramienta de combinación o comprobación compruebe que los módulos de mezcla en conflicto no se combinan en la base de datos del instalador del usuario. La herramienta comprueba haciendo referencia cruzada a esta tabla con la tabla ModuleSignature de la base de datos del instalador.

La tabla ModuleExclusion tiene las siguientes columnas.



| Columna             | Tipo                         | Clave | Nullable |
|--------------------|------------------------------|-----|----------|
| ModuleID           | [Identificador](identifier.md) | Y   | N        |
| ModuleLanguage     | [Entero](integer.md)       | Y   | N        |
| ExcludedID         | [Identificador](identifier.md) | Y   | N        |
| ExcludedLanguage   | [Entero](integer.md)       | Y   | N        |
| ExcludedMinVersion | [Versión](version.md)       |     | Y        |
| ExcludedMaxVersion | [Versión](version.md)       |     | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificador del módulo de combinación. Se trata de una clave externa en la [tabla ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage
</dt> <dd>

Identificador de idioma decimal del módulo de combinación en ModuleID. Se trata de una clave externa en la [tabla ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID
</dt> <dd>

Identificador de un módulo de combinación excluido.

</dd> <dt>

<span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage
</dt> <dd>

Id. de idioma numérico del módulo de combinación en ExcludedID. La columna ExcludedLanguage puede especificar el identificador de idioma de un solo idioma, como 1033 para inglés de EE. UU., o especificar el identificador de idioma de un grupo de idioma, como 9 para cualquier inglés. La columna ExcludedLanguage puede aceptar los id. de idioma negativos. El significado del valor de la columna ExcludedLanguage es el siguiente.



| ExcludedLanguage | Significado                                                              |
|------------------|----------------------------------------------------------------------|
| >0           | Excluya los ID de idioma especificados por ExcludedLanguage.              |
| = 0              | No se excluyen los ID de idioma.                                             |
| < 0           | Excluya todos los ID de idioma excepto los especificados por ExcludedLanguage. |



 

</dd> <dt>

<span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion
</dt> <dd>

Versión mínima excluida de un intervalo. Si el campo ExcludedMinVersion es Null, se excluyen todas las versiones anteriores a ExcludedMaxVersion. Si ExcludedMinVersion y ExcludedMaxVersion son NULL, no hay ninguna exclusión basada en la versión.

</dd> <dt>

<span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion
</dt> <dd>

Versión máxima excluida de un intervalo. Si el campo ExcludedMaxVersion es Null, se excluyen todas las versiones posteriores a ExcludedMinVersion. Si ExcludedMinVersion y ExcludedMaxVersion son NULL, no hay ninguna exclusión basada en la versión.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



