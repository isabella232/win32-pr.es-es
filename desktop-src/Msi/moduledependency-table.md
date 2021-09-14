---
description: La tabla ModuleDependency mantiene una lista de otros módulos de combinación necesarios para que este módulo de combinación funcione correctamente.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: ModuleDependency (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261159"
---
# <a name="moduledependency-table"></a>ModuleDependency (tabla)

La tabla ModuleDependency mantiene una lista de otros módulos de combinación necesarios para que este módulo de combinación funcione correctamente. Esta tabla habilita una herramienta de combinación o comprobación para asegurarse de que los módulos de combinación necesarios se incluyen de hecho en la base de datos del instalador del usuario. La herramienta comprueba haciendo referencia cruzada a esta tabla con la tabla ModuleSignature de la base de datos del instalador.

La tabla ModuleDependency tiene las siguientes columnas.



| Columna           | Tipo                         | Clave | Nullable |
|------------------|------------------------------|-----|----------|
| ModuleID         | [Identificador](identifier.md) | Y   | N        |
| ModuleLanguage   | [Entero](integer.md)       | Y   | N        |
| RequiredID       | [Identificador](identifier.md) | Y   | N        |
| RequiredLanguage | [Entero](integer.md)       | Y   | N        |
| RequiredVersion  | [Versión](version.md)       |     | Y        |



 

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

<span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID
</dt> <dd>

Identificador del módulo de combinación requerido por el módulo de mezcla en ModuleID.

</dd> <dt>

<span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage
</dt> <dd>

Id. de idioma numérico del módulo de combinación en RequiredID. La columna RequiredLanguage puede especificar el identificador de idioma de un solo idioma, como 1033 para inglés de EE. UU., o especificar el identificador de idioma de un grupo de idioma, como 9 para cualquier inglés. Si el campo contiene un identificador de idioma de grupo, cualquier módulo de combinación con un código de idioma en ese grupo satisface la dependencia. Si RequiredLanguage se establece en 0, cualquier módulo de combinación que cumpla los demás requisitos cumplirá la dependencia.

</dd> <dt>

<span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion
</dt> <dd>

Versión del módulo merge en RequiredID. Si este campo es Null, cualquier versión rellena la dependencia.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



