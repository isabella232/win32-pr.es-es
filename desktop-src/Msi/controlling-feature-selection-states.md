---
description: Puede controlar qué opciones de instalación de características están disponibles para que los usuarios y las aplicaciones seleccionen mediante la creación de la tabla de características y la tabla de componentes.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Control de los Estados de selección de características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279010"
---
# <a name="controlling-feature-selection-states"></a>Control de los Estados de selección de características

Puede controlar qué opciones de instalación de características están disponibles para que los usuarios y las aplicaciones seleccionen mediante la creación de la tabla de [características](feature-table.md) y la [tabla de componentes](component-table.md).

-   Para evitar la selección del estado de anuncio de una característica, incluya **msidbFeatureAttributesDisallowAdvertise** en el campo atributos de la característica en la [tabla de características](feature-table.md).
-   Para impedir la selección de los Estados de ejecución desde código fuente o de ejecución desde la red para una característica, incluya **msidbComponentAttributesLocalOnly** en los campos atributos de la [tabla componente](component-table.md) para cada componente que pertenezca a la característica. Si una característica no tiene componentes, la característica siempre tiene las opciones ejecutar desde el origen y ejecutar desde mi equipo disponibles.
-   Para evitar la selección del estado ejecutar desde mi equipo para una característica, incluya **msidbComponentAttributesSourceOnly** en los campos atributos de la [tabla componente](component-table.md) para cada componente que pertenezca a la característica. Si una característica no tiene componentes, la característica siempre tiene las opciones ejecutar desde el origen y ejecutar desde mi equipo disponibles.
-   Se pueden crear nuevas características secundarias incluyendo **msidbFeatureAttributesFollowParent** y **msidbFeatureAttributesUIDisallowAbsent** en el campo atributos de la [tabla de características](feature-table.md).

 

 



