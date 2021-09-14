---
description: La tabla ModuleExclusion mantiene una lista de otros módulos de combinación incompatibles en la misma base de datos del instalador.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: ModuleExclusion Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261151"
---
# <a name="moduleexclusion-table"></a>ModuleExclusion Table

La tabla ModuleExclusion mantiene una lista de otros módulos de combinación incompatibles en la misma base de datos del instalador. Esta tabla permite que una herramienta de combinación o comprobación compruebe que los módulos de combinación en conflicto no se combinan en la base de datos del instalador del usuario. La herramienta comprueba haciendo referencia cruzada a esta tabla con la tabla ModuleSignature de la base de datos del instalador.

La tabla ModuleExclusion tiene las columnas siguientes.



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
| >0           | Excluya los valores de idioma especificados por ExcludedLanguage.              |
| = 0              | No excluya ningún idioma.                                             |
| < 0           | Excluya todos los valores de idioma excepto los especificados por ExcludedLanguage. |



 

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

 

 



