---
title: AccessibleObjectFromPointReturnedNullChildId
description: AccessibleObjectFromPointReturnedNullChildId
ms.assetid: 20511B76-736B-4B43-8DC3-4306DF74CF73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb6ebf33cdfdef7b6e32ec4b9943accc06551d5f37f625fa77cb22e01b913df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994365"
---
# <a name="accessibleobjectfrompointreturnednullchildid"></a>AccessibleObjectFromPointReturnedNullChildId

## <a name="text"></a>Texto

AccessibleObjectFromPoint( {0} , {1} ) devolvió un elemento ChildId nulo

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El elemento ChildId de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto obtenido para las coordenadas dadas es NULL.

## <a name="possible-causes"></a>Causas posibles

La interacción del usuario durante la comprobación, como mover el foco a un HWND no de destino, interfirieron con el proceso de comprobación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegación a través de las pruebas de impacto y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




