---
title: Buscar objetos por clase
description: Consulta de búsqueda típica para una clase de objeto específica.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Buscar objetos por clase AD
- Active Directory, usar, buscar, por clase
- objeto AD, buscar por clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656233"
---
# <a name="finding-objects-by-class"></a><span data-ttu-id="a9c37-106">Buscar objetos por clase</span><span class="sxs-lookup"><span data-stu-id="a9c37-106">Finding Objects by Class</span></span>

<span data-ttu-id="a9c37-107">Consulta de búsqueda típica para una clase de objeto específica.</span><span class="sxs-lookup"><span data-stu-id="a9c37-107">A typical search queries for a specific object class.</span></span> <span data-ttu-id="a9c37-108">En el ejemplo de código siguiente se buscan equipos con ubicación en la compilación de 7N.</span><span class="sxs-lookup"><span data-stu-id="a9c37-108">The following code example searches for computers with location in Building 7N.</span></span>


```C++
(&(objectCategory=computer)(location=Building 7N))
```



<span data-ttu-id="a9c37-109">Tenga en cuenta por qué no se utiliza **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="a9c37-109">Consider why **objectClass** is not used.</span></span> <span data-ttu-id="a9c37-110">No utilice **objectClass** sin otra comparación que contenga un atributo indexado.</span><span class="sxs-lookup"><span data-stu-id="a9c37-110">Do not use **objectClass** without another comparison that contains an indexed attribute.</span></span> <span data-ttu-id="a9c37-111">Los atributos de índice pueden aumentar la eficacia de una consulta.</span><span class="sxs-lookup"><span data-stu-id="a9c37-111">Index attributes can increase the efficiency of a query.</span></span> <span data-ttu-id="a9c37-112">El atributo **objectClass** tiene varios valores y no está indizado.</span><span class="sxs-lookup"><span data-stu-id="a9c37-112">The **objectClass** attribute is multi-valued and not indexed.</span></span> <span data-ttu-id="a9c37-113">Para especificar el tipo o la clase de un objeto, utilice **objectCategory**.</span><span class="sxs-lookup"><span data-stu-id="a9c37-113">To specify the type or class of an object, use **objectCategory**.</span></span>

<span data-ttu-id="a9c37-114">Menos eficaz:</span><span class="sxs-lookup"><span data-stu-id="a9c37-114">Less efficient:</span></span>


```C++
(objectClass=computer)
```



<span data-ttu-id="a9c37-115">Más eficaz:</span><span class="sxs-lookup"><span data-stu-id="a9c37-115">More Efficient:</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="a9c37-116">Tenga en cuenta que hay algunos casos en los que se debe usar una combinación de **objectClass** y **objectCategory** .</span><span class="sxs-lookup"><span data-stu-id="a9c37-116">Be aware that there are some cases where a combination of **objectClass** and **objectCategory** must be used.</span></span> <span data-ttu-id="a9c37-117">La clase de usuario y la clase de contacto deben especificarse como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="a9c37-117">The user class and contact class should be specified as follows.</span></span>


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



<span data-ttu-id="a9c37-118">Tenga en cuenta que puede buscar usuarios y contactos con lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a9c37-118">Be aware that you could search for both users and contacts with the following.</span></span>


```C++
(objectCategory=person)
```



 

 




