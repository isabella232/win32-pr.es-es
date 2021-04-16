---
description: Descripción constante de ICONSTRUCTEDLOCALE de configuración regional \_
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "105995147"
---
# <a name="locale_iconstructedlocale"></a>configuración regional \_ ICONSTRUCTEDLOCALE

Identificador que se va a solicitar si la configuración regional es una configuración regional "construida". No se recomienda el uso de este LCTYPE.

Esto identifica una configuración regional para la que Windows muchos no tienen información completa y tiene que "construir" información en tiempo de ejecución. Normalmente, la información proporcionada por LOCALE_ICONSTRUCTEDLOCALE es de uso limitado ya que Windows proporcionará tantos datos como estén disponibles para cada configuración regional. Por lo tanto, no se recomienda el uso de este LCTYPE.


| Value | Significado                 |
|-------|-------------------------|
| 0     | No construido         |
| 1     | Es una configuración regional construida |


Un ejemplo sería una solicitud de "de-US" o de alemán en el Estados Unidos. NLS usará los datos de idioma alemán que puede encontrar y los datos de la región Estados Unidos que puede encontrar. 

Esto puede no ser perfecto como, por ejemplo, es probable que el sistema no tenga información sobre el nombre de Estados Unidos en alemán. Sin embargo, si la aplicación o el usuario tienen un contexto "de-US", los datos devueltos son los más disponibles. 

Las aplicaciones que usan LOCALE_ICONSTRUCTEDLOCALE para rechazar configuraciones regionales y revertir a una configuración regional diferente suelen acabar con una experiencia peor, como el aterrizaje en la de-DE o en-US en este ejemplo. Ninguno de ellos está cerca de la solicitud original del idioma alemán con una región Estados Unidos.

