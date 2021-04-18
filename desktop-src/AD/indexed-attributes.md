---
title: Atributos indizados (AD DS)
description: Los atributos se pueden indexar. La indización de un atributo puede mejorar el rendimiento de las consultas para ese atributo.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Atributos indizados AD
- Atributos AD, indexados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656333"
---
# <a name="indexed-attributes-ad-ds"></a><span data-ttu-id="38961-106">Atributos indizados (AD DS)</span><span class="sxs-lookup"><span data-stu-id="38961-106">Indexed Attributes (AD DS)</span></span>

<span data-ttu-id="38961-107">Los atributos se pueden indexar.</span><span class="sxs-lookup"><span data-stu-id="38961-107">Attributes may be indexed.</span></span> <span data-ttu-id="38961-108">La indización de un atributo puede mejorar el rendimiento de las consultas para ese atributo.</span><span class="sxs-lookup"><span data-stu-id="38961-108">Indexing an attribute can improve the performance of queries for that attribute.</span></span>

<span data-ttu-id="38961-109">Los atributos se indexan cuando el atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) de la definición de esquema del atributo tiene el bit menos significativo establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="38961-109">An attributes is indexed when the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute in the attribute's schema definition has the least significant bit set to 1.</span></span> <span data-ttu-id="38961-110">Si se establece el bit menos significativo de la definición del esquema del atributo **searchFlags** en 1, se creará un índice de forma dinámica.</span><span class="sxs-lookup"><span data-stu-id="38961-110">Setting the least significant bit of the **searchFlags** attribute schema definition to 1 will dynamically build an index.</span></span> <span data-ttu-id="38961-111">Si se establece el bit menos significativo de la definición del esquema del atributo **searchFlags** en 0, se quitará el índice del atributo.</span><span class="sxs-lookup"><span data-stu-id="38961-111">Setting the least significant bit of the **searchFlags** attribute schema definition to 0 will cause the index for the attribute to be removed.</span></span> <span data-ttu-id="38961-112">Un subproceso en segundo plano generará automáticamente el índice en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="38961-112">The index will be built automatically by a background thread on the domain controller.</span></span>

<span data-ttu-id="38961-113">Idealmente, los atributos indexados deben ser de un solo valor con valores muy únicos distribuidos uniformemente en todo el conjunto de instancias.</span><span class="sxs-lookup"><span data-stu-id="38961-113">Ideally, indexed attributes should be single valued with highly unique values evenly distributed across the set of instances.</span></span> <span data-ttu-id="38961-114">Cuanto menos únicos sean los valores de un atributo, más eficaz será el índice.</span><span class="sxs-lookup"><span data-stu-id="38961-114">The less unique the values of an attribute are, the less effective the index will be.</span></span>

<span data-ttu-id="38961-115">Los atributos con varios valores también se pueden indexar, pero el costo de crear el índice para un atributo con varios valores es mayor en lo que respecta al almacenamiento, la actualización y el tiempo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="38961-115">Multi-valued attributes can also be indexed, but the cost to build the index for a multi-valued attribute is larger in terms of storage, update, and search time.</span></span> <span data-ttu-id="38961-116">El requisito de unicidad de una propiedad con varios valores es el mismo que el de una propiedad de un solo valor. cuanto más únicos son los valores, más efectivo es el índice.</span><span class="sxs-lookup"><span data-stu-id="38961-116">The uniqueness requirement for a multi-valued property is the same as that for a single-valued property—the more unique the values are the more effective the index.</span></span>

<span data-ttu-id="38961-117">Los atributos más indexados que tiene una clase, más tiempo se requiere para crear nuevas instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="38961-117">The more indexed attributes a class has, the more time is required to create new instances of the class.</span></span>

<span data-ttu-id="38961-118">Los índices se aplican a los atributos, no a las clases.</span><span class="sxs-lookup"><span data-stu-id="38961-118">Indexes apply to attributes, not to classes.</span></span> <span data-ttu-id="38961-119">Es decir, cuando un atributo se marca como indizado, todas las instancias del atributo se agregan al índice, no solo las instancias que son miembros de una clase determinada.</span><span class="sxs-lookup"><span data-stu-id="38961-119">That is, when an attribute is marked as indexed, all instances of the attribute are added to the index, not just the instances that are members of a particular class.</span></span>

<span data-ttu-id="38961-120">Para comprobar que un servidor utiliza un índice para procesar una consulta, establezca el siguiente valor del registro en un controlador de dominio en 4.</span><span class="sxs-lookup"><span data-stu-id="38961-120">To verify that a server is using an index to process a query, set the following registry value on a domain controller to 4.</span></span> <span data-ttu-id="38961-121">A continuación, realice una consulta en ese controlador de dominio y busque en el registro de eventos de directorio los datos sobre los índices, si los hay, utilizados para procesar la consulta.</span><span class="sxs-lookup"><span data-stu-id="38961-121">Then perform a query on that domain controller and look in the directory event log for data about the indexes, if any, used to process the query.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

<span data-ttu-id="38961-122">Para obtener más información sobre otros bits en la propiedad [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) , vea [características de los atributos](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="38961-122">For more information about other bits in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) property, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

 

 