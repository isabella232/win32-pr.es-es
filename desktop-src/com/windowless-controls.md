---
title: Controles sin ventana
description: Controles sin ventana
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073035"
---
# <a name="windowless-controls"></a>Controles sin ventana

La especificación ActiveX Controls 96 incluye una definición para los controles sin ventana. Estos controles no funcionan en su propia ventana y requieren que un contenedor ofrezca una ventana compartida en la que se pueda dibujar el control, consulte el SDK ActiveX. Los controles sin ventana están diseñados para ser compatibles con contenedores de control anteriores mediante la creación de su propia ventana en esa situación, los contenedores de controles sin ventanas deben hospedar controles de ventana de la manera tradicional sin ningún problema. Sin embargo, puede ser útil que un contenedor distinga los controles que pueden funcionar en un modo sin ventanas, por lo que se define una categoría de componente adecuada.

CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




