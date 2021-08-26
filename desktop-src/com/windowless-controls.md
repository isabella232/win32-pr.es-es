---
title: Controles sin ventana
description: Controles sin ventana
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf529349a1e1987870b3aac01a69aef3dacbd700d0060cd2177c05479409c7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991995"
---
# <a name="windowless-controls"></a>Controles sin ventana

La ActiveX Controls 96 incluye una definición para controles sin ventanas. Estos controles no funcionan en su propia ventana y requieren que un contenedor ofrezca una ventana compartida en la que se pueda dibujar el control, consulte el SDK de ActiveX. Los controles sin ventanas están diseñados para ser compatibles con contenedores de controles anteriores mediante la creación de su propia ventana en esa situación, los contenedores de controles sin ventanas deben hospedar controles con ventanas de la manera tradicional sin ningún problema. Sin embargo, puede ser útil para un contenedor distinguir los controles que pueden funcionar en un modo sin ventanas, por lo que se define una categoría de componente adecuada.

CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




