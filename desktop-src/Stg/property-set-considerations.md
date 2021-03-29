---
title: Consideraciones sobre los conjuntos de propiedades
description: Se recomienda encarecidamente que los conjuntos de propiedades se mantengan reducidos porque la secuencia del conjunto de propiedades se lee en la memoria antes de que se pueda leer o escribir una sola propiedad.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Consideraciones sobre los conjuntos de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780095"
---
# <a name="property-set-considerations"></a><span data-ttu-id="29cd5-104">Consideraciones sobre los conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="29cd5-104">Property Set Considerations</span></span>

<span data-ttu-id="29cd5-105">Se recomienda encarecidamente que los conjuntos de propiedades se mantengan reducidos porque la secuencia del conjunto de propiedades se lee en la memoria antes de que se pueda leer o escribir una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="29cd5-105">It is strongly recommended that property sets be kept small because the property set stream is read into memory before a single property can be read or written.</span></span> <span data-ttu-id="29cd5-106">"pequeño" significa menos de 32 kilobytes de datos.</span><span class="sxs-lookup"><span data-stu-id="29cd5-106">"small" means less than 32 kilobytes of data.</span></span> <span data-ttu-id="29cd5-107">Esto no suele presentar un problema, ya que, por lo general, las propiedades "en línea" serán elementos pequeños como cadenas descriptivas, palabras clave, marcas de tiempo, recuentos, nombres de autor, identificadores únicos globales (GUID), identificadores de clase (CLSID), etc.</span><span class="sxs-lookup"><span data-stu-id="29cd5-107">This rarely presents a problem because typically, "in-line" properties will be small items such as descriptive strings, keywords, time stamps, counts, author names, globally unique identifiers (GUIDs), class identifiers (CLSIDs), and so forth.</span></span>

<span data-ttu-id="29cd5-108">Para almacenar grandes fragmentos de datos, o en los casos en los que el tamaño total de un conjunto de propiedades relacionadas supere la cantidad recomendada, se recomienda encarecidamente el uso de tipos no simples como el **\_ almacenamiento** **VT \_ Stream** y VT.</span><span class="sxs-lookup"><span data-stu-id="29cd5-108">To store larger chunks of data, or in cases where the total size of a set of related properties far exceeds the recommended amount, the use of nonsimple types such as **VT\_STREAM** and **VT\_STORAGE** are strongly recommended.</span></span> <span data-ttu-id="29cd5-109">No se almacenan en el flujo del conjunto de propiedades, por lo que no afectan de forma significativa a la sobrecarga inicial del primer acceso y la escritura de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="29cd5-109">These are not stored within the property set stream, so they do not significantly affect the initial overhead of the first accessing and writing of a property.</span></span> <span data-ttu-id="29cd5-110">Hay una sobrecarga mínima, ya que la secuencia del conjunto de propiedades contiene el nombre de la propiedad del flujo o del valor de almacenamiento del mismo nivel, lo que tarda en procesarse una pequeña cantidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="29cd5-110">There is a minimal overhead as the property set stream contains the name of the sibling stream- or storage-valued property and this takes an additional small amount of time to process.</span></span>

<span data-ttu-id="29cd5-111">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="29cd5-111">For more information, see:</span></span>

-   [<span data-ttu-id="29cd5-112">Consideraciones de implementación de IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="29cd5-112">IPropertySetStorage Implementation Considerations</span></span>](ipropertysetstorage-implementation-considerations.md)
-   [<span data-ttu-id="29cd5-113">Almacenar conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="29cd5-113">Storing Property Sets</span></span>](storing-property-sets.md)
-   [<span data-ttu-id="29cd5-114">Características de rendimiento</span><span class="sxs-lookup"><span data-stu-id="29cd5-114">Performance Characteristics</span></span>](performance-characteristics.md)
-   [<span data-ttu-id="29cd5-115">Implementar el conjunto de propiedades de información de Resumen</span><span class="sxs-lookup"><span data-stu-id="29cd5-115">Implementing the Summary Information Property Set</span></span>](implementing-the-summary-information-property-set.md)

 

 




