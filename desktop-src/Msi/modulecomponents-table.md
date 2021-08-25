---
description: La tabla ModuleComponents contiene una lista de los componentes que se encuentran en el módulo de combinación.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Tabla ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25216833022ada7592511091c6954222d8ebf354e732c95a54e8857948963541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926485"
---
# <a name="modulecomponents-table"></a>Tabla ModuleComponents

La tabla ModuleComponents contiene una lista de los componentes que se encuentran en el módulo de combinación.

La tabla ModuleComponents tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Componente | [Identificador](identifier.md) | Y   | N        |
| ModuleID  | [Identificador](identifier.md) | Y   | N        |
| Lenguaje  | [Entero](integer.md)       | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Componente
</dt> <dd>

Identificador que hace referencia a un componente en el módulo de combinación. La columna Componente es una clave externa para la [tabla Component](component-table.md). La entrada de la columna Componente debe seguir la convención de nomenclatura en Nomenclatura de claves [principales en bases de datos del módulo de mezcla.](naming-primary-keys-in-merge-module-databases.md)

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificador del módulo de combinación. Se trata de una clave externa para la [tabla ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Lengua
</dt> <dd>

El identificador de idioma describe el idioma predeterminado para el módulo de combinación. El identificador de idioma está en formato decimal, por ejemplo, inglés de EE. UU. es 1033. Clave externa de la [tabla ModuleSignature](modulesignature-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las transformaciones de lenguaje deben ser capaces de actualizar esta tabla si el módulo de combinación admite varios idiomas.

 

 



