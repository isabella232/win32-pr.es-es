---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: AccessibleObjectFromPointReturnedNot \_ S \_ correcto
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85756504520f7d665c1cd1ba7db7c76c1ec5b12a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357146"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>AccessibleObjectFromPointReturnedNot \_ S \_ correcto

## <a name="text"></a>Texto

AccessibleObjectFromPoint ( {0} , {1} ) devuelto {2} y esperado es \_ correcto

## <a name="type"></a>Tipo

Advertencia

## <a name="description"></a>Descripción

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) no devolvió \_ el valor correcto como se esperaba para las coordenadas especificadas.

## <a name="possible-causes"></a>Causas posibles

-   Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.
-   Implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




