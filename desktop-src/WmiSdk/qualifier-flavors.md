---
description: Los tipos de calificador proporcionan más información sobre un calificador, por ejemplo, si una clase derivada o una instancia pueden reemplazar el valor original de los calificadores.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Tipos de calificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707281"
---
# <a name="qualifier-flavors"></a><span data-ttu-id="a1ba7-103">Tipos de calificador</span><span class="sxs-lookup"><span data-stu-id="a1ba7-103">Qualifier Flavors</span></span>

<span data-ttu-id="a1ba7-104">Los tipos de calificador proporcionan más información sobre un calificador, por ejemplo, si una clase derivada o una instancia pueden reemplazar el valor original del calificador.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-104">Qualifier flavors provide more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span>

<span data-ttu-id="a1ba7-105">Se pueden agregar tipos de calificador a la parte superior del archivo MOF mediante la siguiente sintaxis, lo que hace que se apliquen a lo largo de la definición.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-105">Qualifier flavors may be added to the top of the MOF file, using the following syntax, causing them to be applied throughout the definition.</span></span> <span data-ttu-id="a1ba7-106">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a1ba7-106">For example:</span></span>

``` syntax
Qualifier Description : ToSubClass Amended;
```

<span data-ttu-id="a1ba7-107">La **ToSubClass** y los tipos **modificados** se aplican a todos los calificadores de **Descripción** del MOF.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-107">The **ToSubClass** and **Amended** flavors applies to all the **Description** qualifiers in the MOF.</span></span>

<span data-ttu-id="a1ba7-108">En la tabla siguiente se enumeran los tipos de calificador.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-108">The following table lists the qualifier flavors.</span></span>



| <span data-ttu-id="a1ba7-109">Tipo de calificador</span><span class="sxs-lookup"><span data-stu-id="a1ba7-109">Qualifier Flavor</span></span>    | <span data-ttu-id="a1ba7-110">Significado</span><span class="sxs-lookup"><span data-stu-id="a1ba7-110">Meaning</span></span>                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ba7-111">**Modifique**</span><span class="sxs-lookup"><span data-stu-id="a1ba7-111">**Amended**</span></span>         | <span data-ttu-id="a1ba7-112">El calificador no se requiere en la definición de clase básica y puede moverse a la modificación que se va a localizar.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-112">The qualifier is not required in the basic class definition and can be moved to the amendment to be localized.</span></span>                                                                                                                                  |
| <span data-ttu-id="a1ba7-113">**DisableOverride**</span><span class="sxs-lookup"><span data-stu-id="a1ba7-113">**DisableOverride**</span></span> | <span data-ttu-id="a1ba7-114">El calificador no puede invalidarse en una clase o instancia derivada.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-114">The qualifier cannot be overridden in a derived class or instance.</span></span> <span data-ttu-id="a1ba7-115">Tenga en cuenta que el valor predeterminado es poder invalidar un calificador propagado.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-115">Note that being able to override a propagated qualifier is the default.</span></span>                                                                                                      |
| <span data-ttu-id="a1ba7-116">**EnableOverride**</span><span class="sxs-lookup"><span data-stu-id="a1ba7-116">**EnableOverride**</span></span>  | <span data-ttu-id="a1ba7-117">Cuando se propagan a una clase derivada o una instancia, se puede invalidar el valor del calificador.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-117">When propagated to a derived class or instance, the value of the qualifier can be overridden.</span></span> <span data-ttu-id="a1ba7-118">Establecer **EnableOverride** es opcional porque poder invalidar el valor del calificador es la funcionalidad predeterminada para los calificadores propagados.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-118">Setting **EnableOverride** is optional because being able to override the qualifier value is the default functionality for propagated qualifiers.</span></span> |
| <span data-ttu-id="a1ba7-119">**NotToInstance**</span><span class="sxs-lookup"><span data-stu-id="a1ba7-119">**NotToInstance**</span></span>   | <span data-ttu-id="a1ba7-120">El calificador no se propaga a las instancias de clase.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-120">The qualifier is not propagated to class instances.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="a1ba7-121">**NotToSubClass**</span><span class="sxs-lookup"><span data-stu-id="a1ba7-121">**NotToSubClass**</span></span>   | <span data-ttu-id="a1ba7-122">El calificador no se propaga a las clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-122">The qualifier is not propagated to derived classes.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="a1ba7-123">**Restringido**</span><span class="sxs-lookup"><span data-stu-id="a1ba7-123">**Restricted**</span></span>      | <span data-ttu-id="a1ba7-124">El calificador no se propaga a instancias o clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-124">The qualifier is not propagated to instances or derived classes.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="a1ba7-125">**ToInstance**</span><span class="sxs-lookup"><span data-stu-id="a1ba7-125">**ToInstance**</span></span>      | <span data-ttu-id="a1ba7-126">El calificador se propaga a las instancias.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-126">The qualifier is propagated to instances.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="a1ba7-127">**ToSubClass**</span><span class="sxs-lookup"><span data-stu-id="a1ba7-127">**ToSubClass**</span></span>      | <span data-ttu-id="a1ba7-128">El calificador se propaga a las clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-128">The qualifier is propagated to derived classes.</span></span> <span data-ttu-id="a1ba7-129">Este tipo solo es adecuado para los calificadores definidos para una clase y no se puede adjuntar a un calificador que describa una instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="a1ba7-129">This flavor is only appropriate for qualifiers defined for a class and cannot be attached to a qualifier describing a class instance.</span></span>                                                           |



 

 

 



