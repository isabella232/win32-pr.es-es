---
title: objectCategory frente a objectClass
description: Los atributos objectCategory y objectClass pueden hacer referencia a una clase de esquema determinada de un objeto de directorio.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- objectCategory frente a objectClass ADSI
- atributos ASI, buscar en los atributos objectCategory y objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075069"
---
# <a name="objectcategory-vs-objectclass"></a><span data-ttu-id="d5d2b-105">objectCategory frente a objectClass</span><span class="sxs-lookup"><span data-stu-id="d5d2b-105">objectCategory vs. objectClass</span></span>

<span data-ttu-id="d5d2b-106">Los atributos **objectCategory** y **objectClass** pueden hacer referencia a una clase de esquema determinada de un objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="d5d2b-106">Both the **objectCategory** and **objectClass** attributes can refer to a given schema class of a directory object.</span></span> <span data-ttu-id="d5d2b-107">Sin embargo, hay una distinción importante en la semántica entre ambos.</span><span class="sxs-lookup"><span data-stu-id="d5d2b-107">However, there is an important distinction in semantics between the two.</span></span> <span data-ttu-id="d5d2b-108">"objectClass = Joy" hace referencia a estos objetos de directorio en los que "Joy" representa cualquier clase de la jerarquía de clases de objetos.</span><span class="sxs-lookup"><span data-stu-id="d5d2b-108">"objectClass=joy" refers to such directory objects in which "joy" represents any class in the object class hierarchy.</span></span> <span data-ttu-id="d5d2b-109">"objectCategory = Joy", por otro lado, hace referencia a los objetos de directorio en los que "Joy" identifica una clase específica en la jerarquía de clases de objetos.</span><span class="sxs-lookup"><span data-stu-id="d5d2b-109">"objectCategory=joy", on the other hand, refers to those directory objects in which "joy" identifies a specific class in the object class hierarchy.</span></span>

<span data-ttu-id="d5d2b-110">**objectClass** puede tomar varios valores, mientras que **objectCategory** toma un solo valor.</span><span class="sxs-lookup"><span data-stu-id="d5d2b-110">**objectClass** can take multiple values whereas **objectCategory** takes a single value.</span></span> <span data-ttu-id="d5d2b-111">Debido a esto, **objectCategory** es más adecuado para la coincidencia de tipos de objetos en una búsqueda de directorio.</span><span class="sxs-lookup"><span data-stu-id="d5d2b-111">Because of this, **objectCategory** is better suited for type matching of objects in a directory search.</span></span> <span data-ttu-id="d5d2b-112">ADSI lo usa como criterio de coincidencia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d5d2b-112">ADSI uses this as the default matching criterion.</span></span> <span data-ttu-id="d5d2b-113">Las búsquedas que usan un **objectClass** no se pueden escalar a bases de datos grandes.</span><span class="sxs-lookup"><span data-stu-id="d5d2b-113">Searches using one **objectClass** are not scalable to large databases.</span></span> <span data-ttu-id="d5d2b-114">ADSI admite las sintaxis "(objectCategory = SomeDN)" y "(objectCategory \_ = \_ nombre para mostrar de la clase LDAP \_ \_ )".</span><span class="sxs-lookup"><span data-stu-id="d5d2b-114">ADSI supports "(objectCategory=SomeDN)" and "(objectCategory=Ldap\_Display\_Name\_of\_Class)" syntaxes.</span></span>

<span data-ttu-id="d5d2b-115">La excepción a todo esto es que el filtro de búsqueda LDAP "(objectClass = \* )" no especifica una búsqueda en la clase de objeto, sino que simplemente comprueba la presencia de los objetos.</span><span class="sxs-lookup"><span data-stu-id="d5d2b-115">The exception to all of this is that the LDAP search filter "(objectClass=\*)" does not specify a search on object class, but merely tests for the presence of the objects.</span></span>

 

 




