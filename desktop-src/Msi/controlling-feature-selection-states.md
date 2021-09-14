---
description: Puede controlar qué opciones de instalación de características están disponibles para que los usuarios y las aplicaciones seleccionen mediante la creación de la tabla Característica y la tabla De componentes.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Controlar los estados de selección de características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158766"
---
# <a name="controlling-feature-selection-states"></a>Controlar los estados de selección de características

Puede controlar qué opciones de instalación de características están disponibles para que los usuarios y las aplicaciones seleccionen mediante la creación de la tabla [Característica y](feature-table.md) la [tabla componente](component-table.md).

-   Para evitar la selección del estado de anuncio de una característica, incluya **msidbFeatureAttributesDisallowAdvertise** en el campo Atributos de la característica en la [tabla Característica](feature-table.md).
-   Para evitar la selección de los estados run-from-source o run-from-network para una característica, incluya [](component-table.md) **msidbComponentAttributesLocalOnly** en los campos Atributos de la tabla Componente para cada componente que pertenezca a la característica. Si una característica no tiene componentes, la característica siempre tiene disponibles las opciones ejecutar desde el origen y ejecutar desde mi equipo.
-   Para evitar la selección del estado run-from-my-computer de una característica, incluya **msidbComponentAttributesSourceOnly** en los campos Atributos de la tabla Componente para cada componente que pertenezca a la característica. [](component-table.md) Si una característica no tiene componentes, la característica siempre tiene disponibles las opciones ejecutar desde el origen y ejecutar desde mi equipo.
-   Se pueden crear nuevas características secundarias mediante la inclusión de **msidbFeatureAttributesFollowParent** y **msidbFeatureAttributesUIDisallowAbsent** en el campo Atributos de la tabla [Característica](feature-table.md).

 

 



