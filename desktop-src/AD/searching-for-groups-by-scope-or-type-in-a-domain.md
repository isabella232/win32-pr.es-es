---
title: Buscar grupos por ámbito o tipo en un dominio
description: En los dominios de Windows 2000, hay una sola clase denominada Group para todos los ámbitos de grupo (local de dominio, global, universal) y tipos (seguridad, distribución).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Buscar grupos por ámbito o tipo en un dominio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789471"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>Buscar grupos por ámbito o tipo en un dominio

En los dominios de Windows 2000, hay una sola clase denominada [**Group**](/windows/desktop/ADSchema/c-group) para todos los ámbitos de grupo (local de dominio, global, universal) y tipos (seguridad, distribución). El atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) del objeto Group especifica el tipo y el ámbito de grupo.

Para usar el tipo o ámbito para buscar grupos en los dominios de Windows 2000, use un filtro que contenga una regla de coincidencia para el atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) . Para obtener más información sobre las reglas de coincidencia, consulte [Sintaxis de filtro de búsqueda](/windows/desktop/ADSI/search-filter-syntax).

Para obtener más información y un ejemplo de código que muestra cómo buscar grupos en un dominio, consulte el [código de ejemplo para buscar grupos en un dominio](example-code-for-performing-a-query-in-a-domain.md).

## <a name="example-ldap-query-strings"></a>Cadenas de consulta LDAP de ejemplo

Los siguientes ejemplos de cadena de consulta muestran cómo construir una cadena de consulta LDAP que se usa para buscar o filtrar tipos de grupos específicos.

La cadena de consulta siguiente buscará grupos de seguridad. En este ejemplo se usa "-2147483648" como el equivalente decimal de la marca de **\_ \_ \_ seguridad \_ habilitada de tipo de grupo de ADS** .


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



La cadena de consulta siguiente buscará grupos de distribución universales; es decir, los grupos que contienen el tipo de grupo de ADS marca de **\_ \_ \_ \_ grupo universal** y no contienen la marca **seguridad de tipo de grupo de ADS \_ \_ \_ \_ habilitada** . En este ejemplo se usa "8" como el equivalente decimal del grupo universal de tipos de grupos de ADS y "-2147483648" como el equivalente decimal de la marca de **\_ \_ \_ seguridad \_ habilitada de tipo de grupo de ADS** . **\_ \_ \_ \_**


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 