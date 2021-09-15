---
description: Un reconocedor puede encontrar varias maneras de dividir una muestra de lápiz en segmentos de reconocimiento. Por este problema, el número de alternativas de reconocimiento puede ser escalonado, incluso para una pequeña muestra de lápiz.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segmentos de entrada de lápiz y alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572372"
---
# <a name="ink-segments-and-alternates"></a>Segmentos de entrada de lápiz y alternativas

Un reconocedor puede encontrar varias maneras de dividir una muestra de lápiz en segmentos de reconocimiento. Por este problema, el número de alternativas de reconocimiento puede ser escalonado, incluso para una pequeña muestra de lápiz.

Por ejemplo, "t o g e t h e r" puede producir los siguientes resultados:

-   "para obtenerla" (más alternativas para cada palabra)
-   "para recopilar" (más alternativas para cada palabra)
-   "tog ether" (más alternativas para cada palabra)
-   "tog at her" (más alternativas para cada palabra)
-   "together" (más alternativas para la palabra)

El [**objeto RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) admite un almacenamiento eficaz de los resultados de reconocimiento completo dentro del [**objeto Ink.**](inkdisp-class.md) El **objeto Ink** asigna las alternativas de reconocimiento a los trazos del objeto **Ink** y también puede contener otra información, como la posición de línea base, los índices de línea y los intervalos de idioma.

 

 



