---
title: Buscar grupos por ámbito o tipo en un dominio
description: En Windows 2000 dominios, hay una sola clase denominada group para todos los ámbitos de grupo (Dominio local, global, universal) y tipos (seguridad, distribución).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Buscar grupos por ámbito o tipo en un ad de dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d424ce21912aa1e7fa7104099fc8359a5a1c80beeae1fc143aa0bd4aea71d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024953"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>Buscar grupos por ámbito o tipo en un dominio

En Windows 2000 dominios, hay una sola clase denominada [**group**](/windows/desktop/ADSchema/c-group) para todos los ámbitos de grupo (Dominio local, global, universal) y tipos (seguridad, distribución). El [**atributo groupType**](/windows/desktop/ADSchema/a-grouptype) del objeto de grupo especifica el tipo de grupo y el ámbito.

Para usar el tipo o ámbito para buscar grupos en Windows 2000 dominios, use un filtro que contenga una regla de coincidencia para el [**atributo groupType.**](/windows/desktop/ADSchema/a-grouptype) Para obtener más información sobre las reglas de coincidencia, vea [Sintaxis de filtro de búsqueda.](/windows/desktop/ADSI/search-filter-syntax)

Para obtener más información y un ejemplo de código que muestra cómo buscar grupos en un dominio, vea Código de ejemplo para buscar [grupos en un dominio](example-code-for-performing-a-query-in-a-domain.md).

## <a name="example-ldap-query-strings"></a>Cadenas de consulta LDAP de ejemplo

En los siguientes ejemplos de cadenas de consulta se muestra cómo construir una cadena de consulta LDAP que se usa para buscar o filtrar tipos de grupo específicos.

La siguiente cadena de consulta buscará grupos de seguridad. En este ejemplo se usa "-2147483648" como equivalente decimal de la marca **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED.**


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



La siguiente cadena de consulta buscará grupos de distribución universal; es decir, los grupos que contienen la marca **ADS GROUP TYPE UNIVERSAL \_ \_ \_ \_ GROUP** y no contienen la marca **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED.** En este ejemplo se usa "8" como equivalente decimal de **ADS GROUP TYPE UNIVERSAL \_ \_ \_ \_ GROUP** y "-2147483648" como el equivalente decimal de la marca **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED.**


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 