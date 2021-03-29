---
title: Consideraciones de implementación de IPropertySetStorage
description: Al considerar cómo proporcionar una implementación de la interfaz IPropertySetStorage que lee y escribe el formato del conjunto de propiedades COM, surgen varios problemas. En las secciones siguientes se describen estas consideraciones.
ms.assetid: 055da516-ed42-49ec-b20c-a5e98718bea8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7532211668fa1ecf290484a707b19e1c263b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778276"
---
# <a name="ipropertysetstorage-implementation-considerations"></a><span data-ttu-id="ef64b-104">Consideraciones de implementación de IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="ef64b-104">IPropertySetStorage Implementation Considerations</span></span>

<span data-ttu-id="ef64b-105">Al considerar cómo proporcionar una implementación de la interfaz [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) que lee y escribe el formato del conjunto de propiedades com, surgen varios problemas.</span><span class="sxs-lookup"><span data-stu-id="ef64b-105">Several issues arise when considering how to provide an implementation of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface that reads and writes the COM property set format.</span></span> <span data-ttu-id="ef64b-106">En las secciones siguientes se describen estas consideraciones.</span><span class="sxs-lookup"><span data-stu-id="ef64b-106">The following sections describe these considerations.</span></span>

-   [<span data-ttu-id="ef64b-107">Nombres en IStorage</span><span class="sxs-lookup"><span data-stu-id="ef64b-107">Names in IStorage</span></span>](names-in-istorage.md)
-   [<span data-ttu-id="ef64b-108">Objetos de almacenamiento y de secuencia para un conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="ef64b-108">Storage and Stream Objects for a Property Set</span></span>](storage-vs--stream-for-a-property-set.md)
-   [<span data-ttu-id="ef64b-109">Establecimiento del identificador de clase del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="ef64b-109">Setting the Property Set Class Identifier</span></span>](setting-the-property-set-class-identifier.md)
-   [<span data-ttu-id="ef64b-110">Puntos de sincronización</span><span class="sxs-lookup"><span data-stu-id="ef64b-110">Synchronization Points</span></span>](synchronization-points.md)
-   [<span data-ttu-id="ef64b-111">Páginas de códigos y cadenas Unicode</span><span class="sxs-lookup"><span data-stu-id="ef64b-111">Code Pages and Unicode Strings</span></span>](code-pages-and-unicode-strings.md)
-   [<span data-ttu-id="ef64b-112">Diccionario</span><span class="sxs-lookup"><span data-stu-id="ef64b-112">Dictionary</span></span>](dictionary.md)
-   [<span data-ttu-id="ef64b-113">Extensiones</span><span class="sxs-lookup"><span data-stu-id="ef64b-113">Extensions</span></span>](extensions.md)
-   [<span data-ttu-id="ef64b-114">Serialización de conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="ef64b-114">Property Set Serialization</span></span>](version-0-vs--version-1-property-set-serialization.md)

<span data-ttu-id="ef64b-115">Para obtener más información, consulte [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) en la sección de referencia en interfaces.</span><span class="sxs-lookup"><span data-stu-id="ef64b-115">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in the Reference section under Interfaces.</span></span>

 

 




