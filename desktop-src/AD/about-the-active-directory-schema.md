---
title: Acerca del esquema de Active Directory
description: Cada objeto de Active Directory Domain Services es una instancia de una clase de objeto definida en el esquema de Active Directory.
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903005"
---
# <a name="about-the-active-directory-schema"></a><span data-ttu-id="d4896-103">Acerca del esquema de Active Directory</span><span class="sxs-lookup"><span data-stu-id="d4896-103">About the Active Directory Schema</span></span>

<span data-ttu-id="d4896-104">Cada objeto de Active Directory Domain Services es una instancia de una clase de objeto definida en el esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d4896-104">Every object in Active Directory Domain Services is an instance of an object class defined in the Active Directory schema.</span></span> <span data-ttu-id="d4896-105">Una clase de objeto representa una categoría de objetos, como usuarios, impresoras o aplicaciones, que comparten un conjunto de características comunes.</span><span class="sxs-lookup"><span data-stu-id="d4896-105">An object class represents a category of objects, such as users, printers, or application programs, that share a set of common characteristics.</span></span> <span data-ttu-id="d4896-106">La definición de cada clase de objeto contiene una lista de los atributos que se pueden usar para describir instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="d4896-106">The definition for each object class contains a list of the attributes that can be used to describe instances of the class.</span></span> <span data-ttu-id="d4896-107">Por ejemplo, la clase User tiene atributos como **givenName**, **surname** y **streetAddress**.</span><span class="sxs-lookup"><span data-stu-id="d4896-107">For example, the User class has attributes such as **givenName**, **surname**, and **streetAddress**.</span></span> <span data-ttu-id="d4896-108">La lista de atributos de una clase se divide en las que un objeto de esa clase debe contener y los atributos adicionales que puede contener un objeto.</span><span class="sxs-lookup"><span data-stu-id="d4896-108">The list of attributes for a class is divided into those that an object of that class must contain, and additional attributes that an object may contain.</span></span> <span data-ttu-id="d4896-109">El directorio se organiza en una jerarquía; en la definición de cada clase se enumeran también las clases cuyos objetos pueden ser elementos primarios de los objetos de una clase determinada, lo que controla la forma de la jerarquía de directorios.</span><span class="sxs-lookup"><span data-stu-id="d4896-109">The directory is arranged in a hierarchy; the definition of each class also lists the classes whose objects can be parents of objects of a given class—this controls the shape of the directory hierarchy.</span></span>

<span data-ttu-id="d4896-110">El esquema también define formalmente cada atributo.</span><span class="sxs-lookup"><span data-stu-id="d4896-110">The schema also formally defines each attribute.</span></span> <span data-ttu-id="d4896-111">La definición de cada atributo incluye los identificadores únicos del atributo, la sintaxis del atributo (es decir, el tipo de datos para los valores del atributo), los límites de intervalo opcionales para los valores de atributo, si el atributo solo puede tener un valor o varios valores, y si el atributo está indizado.</span><span class="sxs-lookup"><span data-stu-id="d4896-111">The definition for each attribute includes unique identifiers for the attribute, the syntax for the attribute (that is, the data type for the attribute's values), optional range limits for the attribute values, whether the attribute can have only one value or multiple values, and whether the attribute is indexed.</span></span> <span data-ttu-id="d4896-112">El esquema de directorio define cada atributo exactamente una vez: las definiciones de clase de objeto contienen referencias a los atributos definidos en el esquema.</span><span class="sxs-lookup"><span data-stu-id="d4896-112">The directory schema defines each attribute exactly once—object class definitions contain references to the attributes defined in the schema.</span></span> <span data-ttu-id="d4896-113">Por ejemplo, el atributo "Description" solo se define una vez y varias clases de objeto hacen referencia a él.</span><span class="sxs-lookup"><span data-stu-id="d4896-113">For example, the "description" attribute is defined only once and is referenced by many object classes.</span></span> <span data-ttu-id="d4896-114">Esto es diferente de un esquema de base de datos relacional, donde los "atributos" (columnas) se definen por separado para cada tabla.</span><span class="sxs-lookup"><span data-stu-id="d4896-114">This is different than a relational database schema, where the "attributes" (columns) are separately defined for each table.</span></span>

 

 




