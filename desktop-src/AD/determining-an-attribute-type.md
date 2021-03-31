---
title: Determinar un tipo de atributo
description: El atributo systemFlags de un objeto attributeSchema contiene un conjunto de marcas que indican varias cualidades del objeto de atributo, como, por ejemplo, si el atributo está construido o no replicado.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Determinar un tipo de atributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077530"
---
# <a name="determining-an-attribute-type"></a><span data-ttu-id="ad48d-104">Determinar un tipo de atributo</span><span class="sxs-lookup"><span data-stu-id="ad48d-104">Determining an Attribute Type</span></span>

<span data-ttu-id="ad48d-105">El atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) de un objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) contiene un conjunto de marcas que indican varias cualidades del objeto de atributo, como, por ejemplo, si el atributo está construido o no replicado.</span><span class="sxs-lookup"><span data-stu-id="ad48d-105">The [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object contains a set of flags that indicate various qualities of the attribute object, such as whether the attribute is constructed or non-replicated.</span></span> <span data-ttu-id="ad48d-106">En la tabla siguiente se enumeran las marcas del atributo **systemFlags** que afectan al tipo de almacenamiento del atributo.</span><span class="sxs-lookup"><span data-stu-id="ad48d-106">The following table lists the flags of the **systemFlags** attribute that affect the storage type of the attribute.</span></span> 

| <span data-ttu-id="ad48d-107">Valor de marca</span><span class="sxs-lookup"><span data-stu-id="ad48d-107">Flag value</span></span> | <span data-ttu-id="ad48d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad48d-108">Description</span></span>                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad48d-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ad48d-109">0x00000001</span></span> | <span data-ttu-id="ad48d-110">Si esta marca está presente en el atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , el atributo no se replica.</span><span class="sxs-lookup"><span data-stu-id="ad48d-110">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is not replicated.</span></span> |
| <span data-ttu-id="ad48d-111">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ad48d-111">0x00000004</span></span> | <span data-ttu-id="ad48d-112">Si esta marca está presente en el atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , se construye el atributo.</span><span class="sxs-lookup"><span data-stu-id="ad48d-112">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is constructed.</span></span>    |



 

<span data-ttu-id="ad48d-113">Es posible construir una cadena de consulta que se puede usar para consultar atributos construidos o no replicados.</span><span class="sxs-lookup"><span data-stu-id="ad48d-113">It is possible to construct a query string that can be used to query for constructed or non-replicated attributes.</span></span> <span data-ttu-id="ad48d-114">Por ejemplo, la siguiente cadena de consulta busca todos los objetos [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) no replicados.</span><span class="sxs-lookup"><span data-stu-id="ad48d-114">For example, the following query string finds all non-replicated [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects.</span></span> <span data-ttu-id="ad48d-115">Tenga en cuenta que la cadena de consulta requiere el equivalente decimal del valor, no el equivalente hexadecimal del valor.</span><span class="sxs-lookup"><span data-stu-id="ad48d-115">Be aware that the query string requires the decimal equivalent of the value, not the hexadecimal equivalent of the value.</span></span> <span data-ttu-id="ad48d-116">Para obtener más información sobre el OID de la regla de coincidencia que usa esta cadena de consulta, vea [Cómo especificar valores de comparación](how-to-specify-comparison-values.md).</span><span class="sxs-lookup"><span data-stu-id="ad48d-116">For more information about the matching rule OID used by this query string, see [How to Specify Comparison Values](how-to-specify-comparison-values.md).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



<span data-ttu-id="ad48d-117">El atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) del objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo define si un atributo está indizado; un atributo indexado tiene un valor de 1, un atributo no indizado tiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="ad48d-117">The [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is indexed; an indexed attribute has a value of 1, a non-indexed attribute has a value of 0.</span></span> <span data-ttu-id="ad48d-118">Por ejemplo, la siguiente cadena de consulta busca los objetos **attributeSchema** que representan atributos indexados.</span><span class="sxs-lookup"><span data-stu-id="ad48d-118">For example, the following query string finds the **attributeSchema** objects representing indexed attributes.</span></span>


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



<span data-ttu-id="ad48d-119">El atributo [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) del objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo define si un atributo se replica en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="ad48d-119">The [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is replicated to the global catalog.</span></span> <span data-ttu-id="ad48d-120">Este atributo tiene un valor **true** si el atributo es un miembro del catálogo global o **false** si los atributos no están en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="ad48d-120">This attribute has a value of **TRUE** if the attribute is a member of the global catalog or **FALSE** if the attributes is not in the global catalog.</span></span> <span data-ttu-id="ad48d-121">Por ejemplo, la siguiente cadena de consulta busca los objetos **attributeSchema** que se replican en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="ad48d-121">For example, the following query string searches the **attributeSchema** objects that are replicated to the global catalog.</span></span>


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 