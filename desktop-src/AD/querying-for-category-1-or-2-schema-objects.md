---
title: Consulta de objetos de esquema de categoría 1 o 2
description: El atributo systemFlags de los objetos attributeSchema y classSchema es una máscara de máscara de entero que contiene marcas que indican cualidades del sistema adicionales del atributo o la clase.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Consulta de la categoría 1 o 2 objetos de esquema AD
- objeto AD, consulta de objetos de esquema de categoría 1 o 2
- esquema AD, consulta de objetos de esquema de categoría 1 o 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358802"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a><span data-ttu-id="47595-106">Consulta de objetos de esquema de categoría 1 o 2</span><span class="sxs-lookup"><span data-stu-id="47595-106">Querying for Category 1 or 2 Schema Objects</span></span>

<span data-ttu-id="47595-107">El atributo **systemFlags** de los objetos **attributeSchema** y **ClassSchema** es una máscara de máscara de entero que contiene marcas que indican cualidades del sistema adicionales del atributo o la clase.</span><span class="sxs-lookup"><span data-stu-id="47595-107">The **systemFlags** attribute of **attributeSchema** and **classSchema** objects is an integer bitmask that contains flags that indicate additional system qualities of the attribute or class.</span></span> <span data-ttu-id="47595-108">La enumeración de [**\_ \_ enumeración SYSTEMFLAG de ADS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contiene valores que se corresponden con los bits que se pueden establecer en el atributo **systemFlags** .</span><span class="sxs-lookup"><span data-stu-id="47595-108">The [**ADS\_SYSTEMFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) enumeration contains values that correspond to the bits you can set in the **systemFlags** attribute.</span></span> <span data-ttu-id="47595-109">Hay bits de **systemFlags** adicionales que no se pueden establecer, como el bit 0x10, que indica si el atributo o la clase es la categoría 1 o la categoría 2.</span><span class="sxs-lookup"><span data-stu-id="47595-109">There are additional **systemFlags** bits that you cannot set, such as the 0x10 bit which indicates whether the attribute or class is category 1 or category 2.</span></span> <span data-ttu-id="47595-110">El bit 0x10 se establece para objetos de categoría 1, que son las clases y los atributos incluidos en el esquema base incluido con el sistema.</span><span class="sxs-lookup"><span data-stu-id="47595-110">The 0x10 bit is set for category 1 objects, which are the classes and attributes included in the base schema included with the system.</span></span> <span data-ttu-id="47595-111">El bit no está establecido para los atributos y las clases de la categoría 2, que son extensiones del esquema.</span><span class="sxs-lookup"><span data-stu-id="47595-111">The bit is not set for category 2 attributes and classes, which are extensions to the schema.</span></span> <span data-ttu-id="47595-112">Si no existe ninguna propiedad **systemFlags** en un objeto **attributeSchema** o **ClassSchema** , es la categoría 2.</span><span class="sxs-lookup"><span data-stu-id="47595-112">If no **systemFlags** property exists on an **attributeSchema** or **classSchema** object, it is category 2.</span></span>

<span data-ttu-id="47595-113">El **bit de la \_ regla de coincidencia LDAP \_ \_ \_ y** la regla de coincidencia se pueden usar para buscar objetos que tengan la marca 0x10 establecida en el atributo **systemFlags** .</span><span class="sxs-lookup"><span data-stu-id="47595-113">The **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule can be used to search for objects that have the 0x10 flag set in the **systemFlags** attribute.</span></span> <span data-ttu-id="47595-114">Para obtener más información, consulte [Sintaxis de filtro de búsqueda](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="47595-114">For more information, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

## <a name="querying-for-category-1"></a><span data-ttu-id="47595-115">Consulta de categoría 1</span><span class="sxs-lookup"><span data-stu-id="47595-115">Querying for Category 1</span></span>

<span data-ttu-id="47595-116">La siguiente cadena de consulta busca atributos de categoría 1 (objetos **attributeSchema** con el bit 0x10 establecido en la propiedad **systemFlags** ).</span><span class="sxs-lookup"><span data-stu-id="47595-116">The following query string searches for category 1 attributes (**attributeSchema** objects with the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



<span data-ttu-id="47595-117">Tenga en cuenta que, en el ejemplo anterior, la sintaxis de consulta LDAP requiere valores decimales; por lo tanto, el valor hexadecimal de la marca se debe convertir a decimal.</span><span class="sxs-lookup"><span data-stu-id="47595-117">Be aware that, in the example above, the LDAP query syntax requires decimal values; therefore, the hex value of the flag must be converted to decimal.</span></span> <span data-ttu-id="47595-118">En este caso, la categoría 1 bit es 0x10, por lo que el valor de filtro debe especificarse como 16.</span><span class="sxs-lookup"><span data-stu-id="47595-118">In this case, category 1 bit is 0x10 so the filter value must be specified as 16.</span></span>

## <a name="querying-for-category-2"></a><span data-ttu-id="47595-119">Consulta de la categoría 2</span><span class="sxs-lookup"><span data-stu-id="47595-119">Querying for Category 2</span></span>

<span data-ttu-id="47595-120">La siguiente cadena de consulta busca los atributos de categoría 2 (objetos **attributeSchema** que no tienen el bit 0x10 establecido en la propiedad **systemFlags** ).</span><span class="sxs-lookup"><span data-stu-id="47595-120">The following query string searches for category 2 attributes (**attributeSchema** objects that do not have the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



<span data-ttu-id="47595-121">Tenga en cuenta que esta consulta también devuelve objetos **attributeSchema** que no tienen una propiedad **systemFlags** y, por lo tanto, no tienen el marcador especificado establecido implícitamente.</span><span class="sxs-lookup"><span data-stu-id="47595-121">Be aware that this query also returns **attributeSchema** objects that do not have a **systemFlags** property, and, therefore, implicitly do not have the specified flag set.</span></span>

 

 