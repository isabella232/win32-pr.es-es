---
title: Controles sin ventana
description: Controles sin ventana
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419170"
---
# <a name="windowless-controls"></a>Controles sin ventana

La especificación de controles ActiveX 96 incluye una definición de controles sin ventanas. Estos controles no funcionan en su propia ventana y requieren un contenedor para ofrecer una ventana compartida en la que el control puede dibujarse, vea el SDK de ActiveX. Los controles sin ventana están diseñados para ser compatibles con los contenedores de control más antiguos creando su propia ventana en esa situación, los contenedores de control sin ventana deben hospedar controles en ventanas de la forma tradicional sin problemas. Sin embargo, puede ser útil para que un contenedor distinga los controles que pueden funcionar en un modo sin ventanas, por lo que se define una categoría de componente adecuada.

CATId-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATId \_ WindowlessObject

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




