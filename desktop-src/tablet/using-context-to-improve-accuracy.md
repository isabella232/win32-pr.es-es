---
description: Un motor de reconocimiento de escritura a mano, o reconocedor, es un software que procesa la entrada de lápiz y la convierte en texto.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Uso del contexto para mejorar la precisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267583"
---
# <a name="using-context-to-improve-accuracy"></a>Uso del contexto para mejorar la precisión

Un motor de reconocimiento de escritura a mano, o reconocedor, es un software que procesa la entrada de lápiz y la convierte en texto. Un contexto es relevante, información específica de la aplicación que se proporciona a un reconocedor para mejorar la precisión del reconocimiento. En otras palabras, el contexto es cualquier fragmento de información sobre la entrada que ayuda al reconocedor a procesar con precisión la entrada manuscrita en un campo.

En esta sección se describen las distintas formas en que puede aprovechar el contexto en la aplicación tablet PC, y se hace énfasis en la técnica de programación preferida para las aplicaciones que no están habilitadas para la entrada de lápiz.

> [!Note]  
> Hay lugares en las secciones Tecnología de pc de tableta del Kit de desarrollo de software (SDK) de Windows Vista donde se usa el término "contexto" con respecto al objeto [**RecognizerContext**](inkrecognizercontext-class.md) y sus propiedades [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) y [**SuffixText.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) No confunda estos otros usos de "contexto" con la definición de esta sección.

 

 

 



