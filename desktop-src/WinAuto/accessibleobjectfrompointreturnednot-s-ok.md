---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: AccessibleObjectFromPointReturnedNot \_ S \_ OK
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ceabd15e5a401bb67ac14af5a7fb83b96543b4b8046ceee2349d8d57b8de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327692"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>AccessibleObjectFromPointReturnedNot \_ S \_ OK

## <a name="text"></a>Texto

AccessibleObjectFromPoint( {0} , ) devuelto y se esperaba S {1} {2} \_ OK

## <a name="type"></a>Tipo

Advertencia

## <a name="description"></a>Descripción

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) no deseó S \_ OK como se esperaba para las coordenadas dadas.

## <a name="possible-causes"></a>Causas posibles

-   La interacción del usuario durante la comprobación, como mover el foco a un HWND no de destino, interfirieron con el proceso de comprobación.
-   Una implementación de MSAA incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Navegación a través de las pruebas de impacto y la ubicación de la pantalla](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




