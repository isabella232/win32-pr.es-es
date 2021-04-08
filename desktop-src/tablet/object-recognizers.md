---
description: Además de reconocer texto, los reconocedores pueden reconocer una clase de objetos relacionados.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Reconocedores de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002501"
---
# <a name="object-recognizers"></a>Reconocedores de objetos

Además de reconocer texto, los reconocedores pueden reconocer una clase de objetos relacionados. Los reconocedores de objetos reconocen las formas generales según su finalidad. Los reconocedores de objetos se usan para reconocer:

-   Notas musicales
-   Formas geométricas
-   Ecuaciones matemáticas
-   Elementos de diagrama de flujo

Normalmente, los objetos que reconoce este tipo de reconocedor están en una relación funcional o espacial bidimensional entre sí. Por ejemplo, dentro de las relaciones complejas de una ecuación matemática, un reconocedor puede devolver resultados diferentes para un límite superior en un entero definito en lugar de un numerador de una fracción.

Debido a la naturaleza muy general de estas relaciones, es sumamente difícil definir el conjunto de interfaces que funcionarán para cada reconocedor de objetos.

La tecnología de Tablet PC proporciona un marco de trabajo básico para los reconocedores de objetos en la biblioteca administrada y las interfaces de automatización. Sin embargo, debe desarrollar interfaces personalizadas que describan relaciones espaciales complejas entre objetos reconocidos para cada reconocedor de objetos. En concreto, para los reconocedores de objetos, la plataforma proporciona el objeto [**RecognizerContext**](inkrecognizercontext-class.md) básico para asociar el objeto de [**entrada manuscrita**](inkdisp-class.md) con el contexto del reconocedor y para llamar al reconocedor para realizar el reconocimiento.

 

 



