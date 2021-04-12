---
description: El tipo de datos Language es una cadena de texto que contiene uno o más identificadores de idioma numéricos válidos. Si hay dos o más identificadores de idioma, deben separarse con comas.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275436"
---
# <a name="language"></a>Idioma

El tipo de datos Language es una cadena de texto que contiene uno o más identificadores de idioma numéricos válidos. Si hay dos o más identificadores de idioma, deben separarse con comas.

El tipo de datos Language es un valor de 16 bits que es la combinación de los identificadores numéricos principales y de subidioma. El LANGID principal comprende los bits del 0 al 9, mientras que el identificador de subidioma es de bits 10 a 15. Para obtener una lista de los identificadores numéricos principales y secundarios, vea el tema sobre las [constantes y las cadenas de identificador de idioma](../intl/language-identifier-constants-and-strings.md) .

En el caso de los identificadores de idioma principal, el intervalo 0x200 a 0x3ff es definible por el usuario. El intervalo 0x000 a 0x1ff está reservado para el uso del sistema. En el caso de los identificadores de subidioma, el intervalo de 0x20 a 0x3F es definible por el usuario. El intervalo de 0x00 a 0x1F está reservado para uso del sistema.

 

 
