---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71963ad564454dcb90266b4fe4c63ba7282dbc514ab286629798420ff1db9f6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327701"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a>AccessibleObjectFromPointReturnedNullIAccessible

## <a name="text"></a>Texto

AccessibleObjectFromPoint( {0} , {1} ) devolvió null

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

La dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del elemento de interfaz de usuario obtenida para las coordenadas dadas es NULL.

## <a name="possible-causes"></a>Causas posibles

-   La interacción del usuario durante la comprobación, como mover el foco a un HWND no de destino, interfirieron con el proceso de comprobación.
-   Una implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegación a través de las pruebas de impacto y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




