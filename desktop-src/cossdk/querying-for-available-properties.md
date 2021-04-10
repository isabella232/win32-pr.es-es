---
description: Consultar las propiedades disponibles
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Consultar las propiedades disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153388"
---
# <a name="querying-for-available-properties"></a><span data-ttu-id="4e5d4-103">Consultar las propiedades disponibles</span><span class="sxs-lookup"><span data-stu-id="4e5d4-103">Querying for Available Properties</span></span>

<span data-ttu-id="4e5d4-104">Si está escribiendo una herramienta de administración de uso general, lo más probable es que tenga que escribir rutinas para establecer las propiedades en general.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-104">If you are writing a general-purpose administration tool, you most likely will need to write routines for setting properties in full generality.</span></span> <span data-ttu-id="4e5d4-105">Para admitir esto, existe una instalación que permite consultar de forma dinámica las propiedades que están disponibles para los elementos de una colección determinada.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-105">To support this, there is a facility that enables you to dynamically query for the properties that are available for the items in any given collection.</span></span>

<span data-ttu-id="4e5d4-106">La colección [**PropertyInfo**](propertyinfo.md) está disponible en cualquier colección que pueda contener.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-106">The [**PropertyInfo**](propertyinfo.md) collection is available from any collection that you might be holding.</span></span> <span data-ttu-id="4e5d4-107">La colección **PropertyInfo** contiene un elemento para cada propiedad disponible.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-107">The **PropertyInfo** collection contains an item for each available property.</span></span> <span data-ttu-id="4e5d4-108">Puede enumerar estos elementos para determinar si una propiedad determinada está disponible.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-108">You can enumerate through these items to determine whether a given property is available.</span></span>

<span data-ttu-id="4e5d4-109">Puede obtener la colección [**PropertyInfo**](propertyinfo.md) de cualquier colección que esté conservando mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , y dejar en blanco el segundo parámetro, donde normalmente se especificaría la propiedad clave de un elemento primario.</span><span class="sxs-lookup"><span data-stu-id="4e5d4-109">You can get the [**PropertyInfo**](propertyinfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e5d4-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e5d4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e5d4-111">Obtener y establecer propiedades</span><span class="sxs-lookup"><span data-stu-id="4e5d4-111">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="4e5d4-112">Interdependencias entre propiedades</span><span class="sxs-lookup"><span data-stu-id="4e5d4-112">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="4e5d4-113">Guardar o descartar cambios</span><span class="sxs-lookup"><span data-stu-id="4e5d4-113">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



