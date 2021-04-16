---
description: Un motor de reconocimiento de escritura A mano, o reconocedor, es un software que procesa la entrada manuscrita y convierte la entrada manuscrita en texto.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Usar el contexto para mejorar la precisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666481"
---
# <a name="using-context-to-improve-accuracy"></a>Usar el contexto para mejorar la precisión

Un motor de reconocimiento de escritura A mano, o reconocedor, es un software que procesa la entrada manuscrita y convierte la entrada manuscrita en texto. Un contexto es relevante, información específica de la aplicación que se proporciona a un reconocedor para mejorar la precisión del reconocimiento. En otras palabras, el contexto es cualquier parte de la información sobre la entrada que ayuda al reconocedor en el procesamiento preciso de la tinta en un campo.

En esta sección se describen las distintas formas en las que puede aprovechar el contexto de la aplicación de Tablet PC y hacer hincapié en la técnica de programación preferida para las aplicaciones que no están habilitadas para tinta.

> [!Note]  
> Hay lugares en las secciones de tecnología de Tablet PC del kit de desarrollo de software (SDK) de Windows Vista, donde se usa el término "contexto" en relación con el objeto [**RecognizerContext**](inkrecognizercontext-class.md) y sus propiedades [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) y [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) . No confunda estos otros usos de "contexto" con la definición de esta sección.

 

 

 



