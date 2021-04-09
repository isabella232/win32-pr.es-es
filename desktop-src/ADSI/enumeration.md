---
title: Enumeración
description: El acceso a los datos y su manipulación con ADSI proporciona varios ejemplos de enumeración. También puede enumerar los elementos secundarios de los objetos contenedores. Estos elementos secundarios son objetos, en lugar de simplemente propiedades de objetos.
ms.assetid: 1db19b00-8e43-4fc0-9099-1a1135219600
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Visual Basic de código de ejemplo, usar IADsContainer para enumerar objetos
- contenedores ADSI, usar IADsContainer para enumerar los elementos secundarios del contenedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba90e86282939486b79ee09cd17352841e733e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993860"
---
# <a name="enumeration"></a><span data-ttu-id="6d966-107">Enumeración</span><span class="sxs-lookup"><span data-stu-id="6d966-107">Enumeration</span></span>

<span data-ttu-id="6d966-108">El [acceso a los datos y su manipulación con ADSI](accessing-and-manipulating-data-with-adsi.md) proporciona varios ejemplos de enumeración.</span><span class="sxs-lookup"><span data-stu-id="6d966-108">[Accessing and Manipulating Data with ADSI](accessing-and-manipulating-data-with-adsi.md) provides several examples of enumeration.</span></span> <span data-ttu-id="6d966-109">También puede enumerar los elementos secundarios de los objetos contenedores.</span><span class="sxs-lookup"><span data-stu-id="6d966-109">You can also enumerate the children of container objects.</span></span> <span data-ttu-id="6d966-110">Estos elementos secundarios son objetos, en lugar de simplemente propiedades de objetos.</span><span class="sxs-lookup"><span data-stu-id="6d966-110">These children are objects themselves, rather than just properties on objects.</span></span>

<span data-ttu-id="6d966-111">En el ejemplo siguiente se usa la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) para enumerar los elementos secundarios del contenedor.</span><span class="sxs-lookup"><span data-stu-id="6d966-111">The following example uses the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface to enumerate the children of the container.</span></span>


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




