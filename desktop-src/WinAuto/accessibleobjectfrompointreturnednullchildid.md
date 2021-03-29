---
title: AccessibleObjectFromPointReturnedNullChildId
description: AccessibleObjectFromPointReturnedNullChildId
ms.assetid: 20511B76-736B-4B43-8DC3-4306DF74CF73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03c708d13bd8abfe642b99310c8b5bea176e11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779734"
---
# <a name="accessibleobjectfrompointreturnednullchildid"></a>AccessibleObjectFromPointReturnedNullChildId

## <a name="text"></a>Texto

AccessibleObjectFromPoint ( {0} , {1} ) devolvió un ChildId nulo

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

La ChildId de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto obtenida para las coordenadas dadas es NULL.

## <a name="possible-causes"></a>Causas posibles

Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




