---
description: La tabla ModuleComponents contiene una lista de los componentes que se encuentran en el módulo de combinación.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Tabla ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652959"
---
# <a name="modulecomponents-table"></a>Tabla ModuleComponents

La tabla ModuleComponents contiene una lista de los componentes que se encuentran en el módulo de combinación.

La tabla ModuleComponents tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Componente | [Identificador](identifier.md) | Y   | N        |
| ModuleID  | [Identificador](identifier.md) | Y   | N        |
| Idioma  | [Entero](integer.md)       | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Pone
</dt> <dd>

Identificador que hace referencia a un componente en el módulo de combinación. La columna componente es una clave externa de la [tabla de componentes](component-table.md). La entrada de la columna componente debe seguir la Convención de nomenclatura de [asignar nombres a las claves principales de las bases de datos de módulos de combinación](naming-primary-keys-in-merge-module-databases.md).

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificador del módulo de combinación. Se trata de una clave externa de la [tabla ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Módulo
</dt> <dd>

El identificador de idioma describe el idioma predeterminado del módulo de combinación. El identificador de idioma está en formato decimal; por ejemplo, Inglés de EE. UU. es 1033. Clave externa para la [tabla ModuleSignature](modulesignature-table.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las transformaciones del lenguaje deben ser capaces de actualizar esta tabla si el módulo de combinación admite varios idiomas.

 

 



