---
description: El tipo de datos Language es una cadena de texto que contiene uno o varios identificadores de idioma numéricos válidos. Si hay dos o más IDs de idioma, deben estar separados por comas.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Lenguaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071987"
---
# <a name="language"></a>Lenguaje

El tipo de datos Language es una cadena de texto que contiene uno o varios identificadores de idioma numéricos válidos. Si hay dos o más IDs de idioma, deben estar separados por comas.

El tipo de datos Language es un valor de 16 bits que es la combinación de un identificador numérico principal y numérico de sublenguaje. El LANGID principal consta de los bits 0 a 9, mientras que el identificador de sublanguage es bits de 10 a 15. Para obtener una lista de identificadores numéricos principales y de sub language, vea el tema [Language Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md) (Constantes y cadenas de identificador de lenguaje).

En el caso de los id. de idioma principal, el intervalo 0x200 que 0x3ff es definible por el usuario. El intervalo 0x000 que 0x1ff está reservado para el uso del sistema. En el caso de los id. de sublenguaje, el intervalo 0x20 para 0x3f es definible por el usuario. El intervalo 0x00 a 0x1f está reservado para el uso del sistema.

 

 
