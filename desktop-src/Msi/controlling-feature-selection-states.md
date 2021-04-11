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
# <a name="controlling-feature-selection-states"></a><span data-ttu-id="ac1fd-103">Control de los Estados de selección de características</span><span class="sxs-lookup"><span data-stu-id="ac1fd-103">Controlling Feature Selection States</span></span>

<span data-ttu-id="ac1fd-104">Puede controlar qué opciones de instalación de características están disponibles para que los usuarios y las aplicaciones seleccionen mediante la creación de la tabla de [características](feature-table.md) y la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ac1fd-104">You can control which feature installation options are available for users and applications to select by authoring the [Feature table](feature-table.md) and [Component table](component-table.md).</span></span>

-   <span data-ttu-id="ac1fd-105">Para evitar la selección del estado de anuncio de una característica, incluya **msidbFeatureAttributesDisallowAdvertise** en el campo atributos de la característica en la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ac1fd-105">To prevent selection of the advertise state for a feature, include **msidbFeatureAttributesDisallowAdvertise** in the feature's Attributes field in the [Feature table](feature-table.md).</span></span>
-   <span data-ttu-id="ac1fd-106">Para impedir la selección de los Estados de ejecución desde código fuente o de ejecución desde la red para una característica, incluya **msidbComponentAttributesLocalOnly** en los campos atributos de la [tabla componente](component-table.md) para cada componente que pertenezca a la característica.</span><span class="sxs-lookup"><span data-stu-id="ac1fd-106">To prevent selection of the run-from-source or run-from-network states for a feature, include **msidbComponentAttributesLocalOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="ac1fd-107">Si una característica no tiene componentes, la característica siempre tiene las opciones ejecutar desde el origen y ejecutar desde mi equipo disponibles.</span><span class="sxs-lookup"><span data-stu-id="ac1fd-107">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="ac1fd-108">Para evitar la selección del estado ejecutar desde mi equipo para una característica, incluya **msidbComponentAttributesSourceOnly** en los campos atributos de la [tabla componente](component-table.md) para cada componente que pertenezca a la característica.</span><span class="sxs-lookup"><span data-stu-id="ac1fd-108">To prevent selection of the run-from-my-computer state for a feature, include **msidbComponentAttributesSourceOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="ac1fd-109">Si una característica no tiene componentes, la característica siempre tiene las opciones ejecutar desde el origen y ejecutar desde mi equipo disponibles.</span><span class="sxs-lookup"><span data-stu-id="ac1fd-109">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="ac1fd-110">Se pueden crear nuevas características secundarias incluyendo **msidbFeatureAttributesFollowParent** y **msidbFeatureAttributesUIDisallowAbsent** en el campo atributos de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ac1fd-110">New child features can be authored by including **msidbFeatureAttributesFollowParent** and **msidbFeatureAttributesUIDisallowAbsent** in the Attributes field of the [Feature table](feature-table.md).</span></span>

 

 



