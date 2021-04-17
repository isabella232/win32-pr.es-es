---
title: Espacio de nombres
description: Un espacio de nombres es un contexto en el que los nombres de todos los objetos deben poder resolverse sin ambigüedades.
ms.assetid: 7731f6b5-1efa-43bc-bd31-9b5183ec90dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb79ba44bfaab1ea50dd89961503176dc8fbd1a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105660091"
---
# <a name="namespace"></a>Espacio de nombres

Un espacio de nombres es un contexto en el que los nombres de todos los objetos deben poder resolverse sin ambigüedades. Por ejemplo, Internet es un solo espacio de nombres DNS, en el que todos los dispositivos de red con un nombre DNS se pueden resolver en una dirección determinada (por ejemplo, se `www.microsoft.com` resuelve como 207.46.131.13).

## <a name="flat-namespace"></a>Espacio de nombres plano

Un espacio de nombres puede ser plano o jerárquico. Un espacio de nombres plano no se escala bien porque puede crecer tan solo hasta que se usen todos los nombres disponibles. Una vez que un nombre se usa más de una vez en un espacio de nombres, el espacio de nombres infringe el requisito que se pueda resolver de forma inequívoca.

## <a name="hierarchical-namespace"></a>Espacio de nombres jerárquico

Un espacio de nombres jerárquico se divide en áreas diferentes, que se pueden considerar como subespacios de nombres. Cada área es su propio subespacio de nombres dentro del espacio de nombres global. Por lo tanto, cada objeto solo debe tener un nombre único dentro de su subespacio de nombres para tener un nombre que se pueda resolver de forma no ambigua dentro de la jerarquía de espacios de nombres. Los espacios de nombres jerárquicos, a continuación, se pueden escalar a redes extremadamente grandes a &mdash; medida que se agregan más objetos al espacio de nombres global, hay que buscar nombres únicos para ellos solo en el subespacio de nombres al que pertenecen.

Todos los espacios de nombres DNS son jerárquicos. Los subespacios de nombres del espacio de nombres jerárquico DNS se denominan *dominios*. El nombre único de un equipo dentro de un dominio se denomina *nombre distintivo relativo*. Los equipos con el mismo nombre distintivo relativo pueden existir en diferentes subespacios de nombres (dominios) de la jerarquía de espacios de nombres porque se pueden resolver por completo en un objeto único dentro de toda la jerarquía de DNS, utilizando un nombre de dominio completo (FQDN). Por ejemplo, podría tener un servidor denominado *server1* en el dominio *widgets.Microsoft.com* (el espacio de nombres *widgets.Microsoft.com* ) y podría tener *server1* en el espacio de nombres *gadgets.widgets.Microsoft.com* . Dado que se encuentran en distintos espacios de nombres en el espacio de nombres jerárquico, se pueden resolver en diferentes FQDN &mdash; *server1.widgets.microsoft.com* y *server1.gadgets.widgets.Microsoft.com*.
