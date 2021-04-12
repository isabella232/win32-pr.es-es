---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c5807fa04f69271f2a2d38e7014b1cd17d4eaa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357670"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a>AccessibleObjectFromPointReturnedNullIAccessible

## <a name="text"></a>Texto

AccessibleObjectFromPoint ( {0} , {1} ) devolvió null

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

La dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del elemento de la interfaz de usuario obtenida para las coordenadas dadas es NULL.

## <a name="possible-causes"></a>Causas posibles

-   Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.
-   Implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




