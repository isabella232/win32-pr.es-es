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
# <a name="enumeration"></a>Enumeración

El [acceso a los datos y su manipulación con ADSI](accessing-and-manipulating-data-with-adsi.md) proporciona varios ejemplos de enumeración. También puede enumerar los elementos secundarios de los objetos contenedores. Estos elementos secundarios son objetos, en lugar de simplemente propiedades de objetos.

En el ejemplo siguiente se usa la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) para enumerar los elementos secundarios del contenedor.


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




