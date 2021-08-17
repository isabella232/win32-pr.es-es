---
description: Además de reconocer texto, los reconocedores pueden reconocer una clase de objetos relacionados.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Reconocedores de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabfd44a5eb126d48df70efd1c391584d12afc94e5e21c714aa0c740a7d486f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449666"
---
# <a name="object-recognizers"></a>Reconocedores de objetos

Además de reconocer texto, los reconocedores pueden reconocer una clase de objetos relacionados. Los reconocedores de objetos reconocen formas generales, según su propósito. Los reconocedores de objetos se usan para reconocer:

-   Notas de música
-   Formas geométricas
-   Ecuaciones matemáticas
-   Flow de gráfico

Normalmente, los objetos reconocidos por este reconocedor están en una relación espacial o funcional bidimensional entre sí. Por ejemplo, dentro de las relaciones complejas de una ecuación matemática, un reconocedor puede devolver resultados diferentes para un límite superior en un entero definido en lugar de un numerador en una fracción.

Debido a la naturaleza muy general de estas relaciones, es muy difícil definir el conjunto de interfaces que funcionarán para cada reconocedor de objetos.

La tecnología de pc de tableta proporciona un marco básico para los reconocedores de objetos en las interfaces de automatización y biblioteca administrada. Sin embargo, debe desarrollar interfaces personalizadas que describan relaciones espaciales complejas entre objetos reconocidos para cada reconocedor de objetos. En concreto, para los reconocedores de objetos, la plataforma proporciona el objeto [**RecognizerContext**](inkrecognizercontext-class.md) básico para asociar el objeto [**Ink**](inkdisp-class.md) al contexto del reconocedor y para llamar al reconocedor para realizar el reconocimiento.

 

 



