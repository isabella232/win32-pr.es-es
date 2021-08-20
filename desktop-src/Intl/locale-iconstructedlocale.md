---
description: ICONO DE \_ CONFIGURACIÓN REGIONALSTRUCTEDLOCALE descripción de la constante
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 26d54ce55393f54d56f521231e257a8b0692758f8e6c830a890d81c8f82e8422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809643"
---
# <a name="locale_iconstructedlocale"></a>ICONO DE \_ CONFIGURACIÓN REGIONALSTRUCTEDLOCALE

Identificador que se va a solicitar si la configuración regional es una configuración regional "construida". No se recomienda usar este LCTYPE.

Esto identifica una configuración regional para la que muchos Windows tienen información completa y tienen que "construir" información en tiempo de ejecución. Normalmente, la información proporcionada por LOCALE_ICONSTRUCTEDLOCALE es de uso limitado, ya que Windows proporcionará tantos datos como estén disponibles para cada configuración regional. Por lo tanto, no se recomienda usar este LCTYPE.


| Value | Significado                 |
|-------|-------------------------|
| 0     | No construido         |
| 1     | Es una configuración regional construida |


Un ejemplo sería una solicitud de "de-US" o alemán en la Estados Unidos. NLS usará los datos en alemán que puede encontrar y los datos de Estados Unidos región que puede encontrar. 

Esto puede no ser perfecto, ya que, por ejemplo, es probable que el sistema no tenga información sobre el nombre de Estados Unidos en alemán. Sin embargo, si la aplicación o el usuario desean un contexto "de-US", los datos devueltos son los mejores disponibles. 

Las aplicaciones que usan LOCALE_ICONSTRUCTEDLOCALE rechazar configuraciones regionales y volver a una configuración regional diferente suelen acabar con una experiencia peor, como el aterrizaje en de-DE o en-US en este ejemplo. Ninguno de ellos está cerca de la solicitud original para el idioma alemán con una Estados Unidos región.

