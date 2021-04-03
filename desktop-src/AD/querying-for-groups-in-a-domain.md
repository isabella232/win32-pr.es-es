---
title: Consultar los grupos de un dominio
description: Los grupos se pueden colocar en cualquier contenedor o unidad organizativa de un dominio, así como en la raíz del dominio.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Consulta de grupos en un dominio de Active Directory
- Agrupa AD, consultar los grupos de un dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904476"
---
# <a name="querying-for-groups-in-a-domain"></a>Consultar los grupos de un dominio

Los grupos se pueden colocar en cualquier contenedor o unidad organizativa de un dominio, así como en la raíz del dominio. Es posible que los grupos no siempre estén en un contenedor. Por lo tanto, es necesario buscar en todo el dominio para buscar todos los grupos del dominio.

Para buscar todos los grupos de un dominio, establezca el punto de inicio de la búsqueda en la raíz del dominio, establezca el ámbito de búsqueda en subárbol y busque todos los objetos que tengan un valor de [**objectClass**](/windows/desktop/ADSchema/a-objectclass) de "grupo".

Si se deben encontrar grupos que contienen valores de [**\_ \_ \_ enumeración de tipo de grupo de anuncios**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) concretos, se pueden usar el bit de regla de coincidencia de **LDAP \_ \_ \_ \_ y** el operador de regla de coincidencia para buscar grupos que tengan determinados bits establecidos en el atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) . Para obtener más información sobre el uso de reglas de coincidencia, consulte [Sintaxis de filtro de búsqueda](/windows/desktop/ADSI/search-filter-syntax).

Para obtener más información y un ejemplo de código que muestra cómo buscar grupos en un dominio, consulte el [código de ejemplo para buscar grupos en un dominio](example-code-for-performing-a-query-in-a-domain.md).

 

 