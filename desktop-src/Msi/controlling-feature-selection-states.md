---
description: Puede controlar qué opciones de instalación de características están disponibles para que los usuarios y las aplicaciones seleccionen mediante la creación de la tabla De características y la Tabla de componentes.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Controlar los estados de selección de características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd269e5b7b0c810df6f7f0909d56b98cdd1c54c9b51eacc40656fe48fc32f8e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379910"
---
# <a name="controlling-feature-selection-states"></a>Controlar los estados de selección de características

Puede controlar qué opciones de instalación de características están disponibles para que los usuarios y las aplicaciones seleccionen mediante la creación de la tabla [Característica y](feature-table.md) la [tabla Componente](component-table.md).

-   Para evitar la selección del estado de anuncio de una característica, incluya **msidbFeatureAttributesDisallowAdvertise** en el campo Atributos de la característica en la [tabla Característica](feature-table.md).
-   Para evitar la selección de los estados run-from-source o run-from-network para una característica, incluya [](component-table.md) **msidbComponentAttributesLocalOnly** en los campos Atributos de la tabla Component para cada componente que pertenezca a la característica. Si una característica no tiene componentes, la característica siempre tiene las opciones ejecutar desde el origen y ejecutar desde mi equipo disponibles.
-   Para evitar la selección del estado de ejecución desde mi equipo para una característica, incluya **msidbComponentAttributesSourceOnly** en los campos Atributos de la tabla Componente para cada componente que pertenezca a la característica. [](component-table.md) Si una característica no tiene componentes, la característica siempre tiene las opciones ejecutar desde el origen y ejecutar desde mi equipo disponibles.
-   Se pueden crear nuevas características secundarias incluyendo **msidbFeatureAttributesFollowParent** y **msidbFeatureAttributesUIDisallowAbsent** en el campo Atributos de la [tabla Característica](feature-table.md).

 

 



