---
description: Un motor de reconocimiento de escritura a mano, o reconocedor, es un software que procesa la entrada de lápiz y la convierte en texto.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Uso del contexto para mejorar la precisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7564c18ace39c17e8877c3e5edee6464caea0c36d148cffbfcfb3b5ac09f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715279"
---
# <a name="using-context-to-improve-accuracy"></a>Uso del contexto para mejorar la precisión

Un motor de reconocimiento de escritura a mano, o reconocedor, es un software que procesa la entrada de lápiz y la convierte en texto. Un contexto es relevante, información específica de la aplicación que se proporciona a un reconocedor para mejorar la precisión del reconocimiento. En otras palabras, el contexto es cualquier fragmento de información sobre la entrada que ayuda al reconocedor a procesar con precisión la entrada manuscrita en un campo.

En esta sección se describen las distintas formas de aprovechar el contexto en la aplicación de Tablet PC, y se pone énfasis en la técnica de programación preferida para las aplicaciones que no tienen habilitada la entrada de lápiz.

> [!Note]  
> Hay lugares en las secciones Tecnología de pc de tableta del Kit de desarrollo de software (SDK) de Windows Vista en los que se usa el término "contexto" con respecto al objeto [**RecognizerContext**](inkrecognizercontext-class.md) y sus propiedades [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) y [**SuffixText.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) No confunda estos otros usos de "contexto" con la definición de esta sección.

 

 

 



