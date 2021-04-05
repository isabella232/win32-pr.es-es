---
description: Un reconocedor puede encontrar varias maneras de dividir una muestra de entrada manuscrita en segmentos de reconocimiento. Por este motivo, el número de alternativas de reconocimiento puede ser escalonado, incluso para una pequeña muestra de tinta.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segmentos de tinta y alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082095"
---
# <a name="ink-segments-and-alternates"></a>Segmentos de tinta y alternativas

Un reconocedor puede encontrar varias maneras de dividir una muestra de entrada manuscrita en segmentos de reconocimiento. Por este motivo, el número de alternativas de reconocimiento puede ser escalonado, incluso para una pequeña muestra de tinta.

Por ejemplo, "t o g e t h e r" puede producir los siguientes resultados:

-   "para obtener" (más alternativas para cada palabra)
-   "para recopilar" (más alternativas para cada palabra)
-   "TOG ether" (más alternativas para cada palabra)
-   "TOG" (más alternativas para cada palabra)
-   "juntos" (más alternativas para la palabra)

El objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) admite el almacenamiento eficaz de los resultados de reconocimiento completo en el objeto de [**entrada manuscrita**](inkdisp-class.md) . El objeto de **entrada manuscrita** asigna las alternativas de reconocimiento a los trazos del objeto de **entrada manuscrita** y puede contener también otra información, como la posición de línea base, los índices de línea e intervalos de idioma.

 

 



