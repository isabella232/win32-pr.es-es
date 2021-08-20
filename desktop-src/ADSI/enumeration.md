---
title: Enumeración
description: El acceso y la manipulación de datos con ADSI proporciona varios ejemplos de enumeración. También puede enumerar los elementos secundarios de los objetos de contenedor. Estos secundarios son objetos en sí mismos, en lugar de solo propiedades en objetos .
ms.assetid: 1db19b00-8e43-4fc0-9099-1a1135219600
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, código de ejemplo Visual Basic , mediante IADsContainer para enumerar objetos
- containers ADSI , mediante IADsContainer para enumerar los elementos secundarios del contenedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7991719c6cd546f02c2f3c4ed18830fc6187b2c9c8603aee9014ec69a14604b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017605"
---
# <a name="enumeration"></a>Enumeración

[El acceso y la manipulación de datos con ADSI](accessing-and-manipulating-data-with-adsi.md) proporciona varios ejemplos de enumeración. También puede enumerar los elementos secundarios de los objetos de contenedor. Estos secundarios son objetos en sí mismos, en lugar de solo propiedades en objetos .

En el ejemplo siguiente se usa [**la interfaz IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) para enumerar los elementos secundarios del contenedor.


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




