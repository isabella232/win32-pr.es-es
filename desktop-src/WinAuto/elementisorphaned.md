---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf30478d7ca68f823cd3d87158f92af71ae1afb14bf8d17295eedee2b4a144d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829381"
---
# <a name="elementisorphaned"></a>ElementIsOrphaned

## <a name="text"></a>Texto

El elemento es un IAccessible huérfano en el árbol.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

La dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto obtenida para las coordenadas dadas es una referencia a un elemento huérfano en el árbol de elementos.

Este problema es un problema para las personas que dependen de un lector de pantalla y un teclado para la navegación porque los elementos se tratarán como invisibles y no se anunciarán al usuario.

## <a name="possible-causes"></a>Causas posibles

-   La interacción del usuario durante la comprobación, como mover el foco a un HWND no de destino, interfirieron con el proceso de comprobación.
-   Una implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegación a través de las pruebas de impacto y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




