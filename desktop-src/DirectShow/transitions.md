---
description: Transiciones
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7511a010de60cdd87907b4ad7faa59963d3f0c6037dce3adc8fc58fa1c0a67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078715"
---
# <a name="transitions"></a>Transiciones

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Una transición es una manera de segue de una pista de vídeo a otra, mediante un efecto visual como una atenuación o un borrado. En la ilustración siguiente se muestra una escala de tiempo con una transición:

![escala de tiempo con transición](images/timeline3.png)

El objeto de transición está en la pista 1 y representa una transición de la pista 0 a la pista 1. Al principio de la transición, el vídeo representado es completamente de La pista 0 (origen A). Al final, el vídeo es totalmente de la pista 1 (origen C). En el medio, la salida pasa del origen A al origen C. Por ejemplo, en una transición de atenuación, un origen se atenua progresivamente al otro. La salida final se esquematiza en la parte inferior de la ilustración.

Las transiciones no se pueden superponer en el tiempo dentro de la misma pista, pero puede crear transiciones superpuestas mediante el objeto de composición, como se describe en [Composición y capas.](composition-and-layering.md)

Una transición tiene una dirección. De forma predeterminada, comienza desde la pista de prioridad inferior (origen A, en el ejemplo anterior) y termina en la pista de prioridad más alta (origen C). En el medio, el vídeo es una combinación de los dos orígenes. Sin embargo, puede especificar el comportamiento opuesto, como se muestra en la ilustración siguiente:

![ntrack con dos transiciones](images/fade.png)

En este caso, la primera transición desaparece de la pista 0 y se atenua la pista 1, que es el comportamiento predeterminado. La segunda transición pasa de la pista 1 a la pista 0. Tenga en cuenta que ambas transiciones se encuentran en la pista 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con DirectShow Editing Services](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Transiciones y efectos](transitions-and-effects.md)
</dt> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



