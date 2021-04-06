---
description: Los módulos de combinación solo funcionan con componentes y no con características. Sin embargo, algunas tablas de los módulos de combinación, como la tabla PublishComponent, contienen campos que hacen referencia a las características de.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Hacer referencia a características en módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001872"
---
# <a name="referencing-features-in-merge-modules"></a><span data-ttu-id="bf58f-104">Hacer referencia a características en módulos de combinación</span><span class="sxs-lookup"><span data-stu-id="bf58f-104">Referencing Features in Merge Modules</span></span>

<span data-ttu-id="bf58f-105">Los módulos de combinación solo funcionan con componentes y no con características.</span><span class="sxs-lookup"><span data-stu-id="bf58f-105">Merge modules only operate with components and not with features.</span></span> <span data-ttu-id="bf58f-106">Sin embargo, algunas tablas de los módulos de combinación, como la [tabla PublishComponent](publishcomponent-table.md), contienen campos que hacen referencia a las características de.</span><span class="sxs-lookup"><span data-stu-id="bf58f-106">However, some tables in merge modules, such as the [PublishComponent table](publishcomponent-table.md), contain fields that refer to features.</span></span>

<span data-ttu-id="bf58f-107">Un GUID NULL: {00000000-0000-0000-0000-000000000000} se debe crear en cualquier campo de una base de datos de módulo de combinación que haga referencia a una característica.</span><span class="sxs-lookup"><span data-stu-id="bf58f-107">A null GUID: {00000000-0000-0000-0000-000000000000} must be authored into any field of a merge module database that references a feature.</span></span> <span data-ttu-id="bf58f-108">Cuando el módulo de fusión mediante combinación se combina en un paquete de instalación, la herramienta de combinación reemplaza el GUID nulo con la característica especificada en el paquete de instalación, excepto en las tablas que requieren un tratamiento especial, como la [tabla ModuleSignature](modulesignature-table.md) y las tablas ModuleSequence.</span><span class="sxs-lookup"><span data-stu-id="bf58f-108">When the merge module is merged into an installation package, the merge tool replaces the null GUID with the feature specified in the installation package, except for tables that require special handling, such as the [ModuleSignature table](modulesignature-table.md) and the ModuleSequence tables.</span></span>

<span data-ttu-id="bf58f-109">Tenga en cuenta que si se usa un GUID NULL como clave principal, no se garantiza que el valor que sustituye a la herramienta de combinación sea único.</span><span class="sxs-lookup"><span data-stu-id="bf58f-109">Note that if a null GUID is used as a primary key, it is not guaranteed that the value substituted by the merge tool is unique.</span></span> <span data-ttu-id="bf58f-110">Los autores de los módulos de combinación son los responsables de garantizar que no se duplique ninguna clave principal existente en la interfaz del usuario cuando la herramienta de fusión mediante combinación Reemplace los GUID nulos por las características de.</span><span class="sxs-lookup"><span data-stu-id="bf58f-110">Authors of merge modules are responsible for ensuring that no existing primary key in the user's interface is duplicated when the merge tool replaces null GUIDs with features.</span></span>

 

 



