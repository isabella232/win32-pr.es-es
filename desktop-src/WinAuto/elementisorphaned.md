---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704805"
---
# <a name="elementisorphaned"></a>ElementIsOrphaned

## <a name="text"></a>Texto

El elemento es un IAccessible huérfano en el árbol

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

La dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto obtenida para las coordenadas especificadas es una referencia a un elemento huérfano en el árbol de elementos.

Este problema es un problema para las personas que confían en un lector de pantalla y un teclado para la navegación, ya que los elementos se tratarán como invisibles y no se anunciarán al usuario.

## <a name="possible-causes"></a>Causas posibles

-   Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.
-   Implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




