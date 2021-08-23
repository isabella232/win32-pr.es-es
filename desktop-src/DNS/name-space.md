---
title: Espacio de nombres
description: Un espacio de nombres es un contexto en el que los nombres de todos los objetos deben poder resolverse de forma inequívoca.
ms.assetid: 7731f6b5-1efa-43bc-bd31-9b5183ec90dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce9119b49cde888cb51f65e6e6b677fb364d640e1b78fe48c739b7c1206936d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692205"
---
# <a name="namespace"></a>Espacio de nombres

Un espacio de nombres es un contexto en el que los nombres de todos los objetos deben poder resolverse de forma inequívoca. Por ejemplo, Internet es un espacio de nombres DNS único, en el que todos los dispositivos de red con un nombre DNS se pueden resolver en una dirección determinada (por ejemplo, se resuelve en `www.microsoft.com` 207.46.131.13).

## <a name="flat-namespace"></a>Espacio de nombres plano

Un espacio de nombres puede ser plano o jerárquico. Un espacio de nombres plano no se escala bien porque solo puede crecer tan grande antes de que se utilicen todos los nombres disponibles. Una vez que se usa un nombre más de una vez en un espacio de nombres, el espacio de nombres infringe el requisito inequívoco de resolución.

## <a name="hierarchical-namespace"></a>Espacio de nombres jerárquico

Un espacio de nombres jerárquico se divide en distintas áreas, que se pueden pensar como subcompartidos. Cada área es su propio sub namespace dentro del espacio de nombres general. Por lo tanto, cada objeto debe tener un nombre único solo dentro de su sub namespace para tener un nombre que se pueda resolver de forma inequívoca dentro de la jerarquía de espacios de nombres. Los espacios de nombres jerárquicos, a continuación, se pueden escalar a redes extremadamente grandes a medida que agrega más objetos al espacio de nombres general; solo tiene que buscar nombres únicos para ellos dentro del subconsóso de nombres al que &mdash; pertenecen.

Todos los espacios de nombres DNS son jerárquicos. Los sub namespaces del espacio de nombres jerárquico DNS se *denominan dominios*. El nombre único de un equipo dentro de un dominio se denomina *nombre distintivo relativo.* Los equipos con el mismo nombre distintivo relativo pueden existir en diferentes subnodos (dominios) de la jerarquía de espacios de nombres porque se pueden resolver completamente en un objeto único dentro de toda la jerarquía DNS, mediante un nombre de dominio completo (FQDN). Por ejemplo, podría tener un servidor denominado *server1* en el dominio *widgets.microsoft.com* (el espacio de nombres *widgets.microsoft.com)* y podría tener *server1* en el espacio de nombres *gadgets.widgets.microsoft.com* servidor. Dado que se encuentran en diferentes subnodos del espacio de nombres jerárquico, se pueden resolver en distintos FQDN &mdash; *server1.widgets.microsoft.com* y *server1.gadgets.widgets.microsoft.com*.
