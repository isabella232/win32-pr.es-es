---
description: El tipo de datos Language es una cadena de texto que contiene uno o varios identificadores de idioma numéricos válidos. Si hay dos o más iDs de idioma, deben estar separados por comas.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Lenguaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b98e24ec0ad4d4b42dfcba02374792e10ea117db474a973eae06336a55834538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013133"
---
# <a name="language"></a>Lenguaje

El tipo de datos Language es una cadena de texto que contiene uno o varios identificadores de idioma numéricos válidos. Si hay dos o más iDs de idioma, deben estar separados por comas.

El tipo de datos Language es un valor de 16 bits que es la combinación de identificadores numéricos principales y de subidioma. El LANGID principal consta de los bits 0 a 9, mientras que el identificador de subLanguage es de bits 10 a 15. Para obtener una lista de identificadores numéricos principales y de subnúblio, vea el tema Constantes y [cadenas](../intl/language-identifier-constants-and-strings.md) de identificador de idioma.

En el caso de los id. de idioma principal, el 0x200 que 0x3ff es definible por el usuario. El intervalo 0x000 a 0x1ff está reservado para uso del sistema. En el caso de los id. de subidioma, el intervalo 0x20 que 0x3f es definible por el usuario. El intervalo 0x00 a 0x1f está reservado para uso del sistema.

 

 
