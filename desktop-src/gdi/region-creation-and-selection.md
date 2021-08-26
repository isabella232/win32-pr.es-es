---
description: Una aplicación crea una región mediante una llamada a una función asociada a una forma específica. En la tabla siguiente se muestran las funciones asociadas a cada una de las formas estándar.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Creación y selección de regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ce2711b2d1ae9dc6641748c72fd586d02e25964102a8c034593d6e60cbaa33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092695"
---
# <a name="region-creation-and-selection"></a>Creación y selección de regiones

Una aplicación crea una región mediante una llamada a una función asociada a una forma específica. En la tabla siguiente se muestran las funciones asociadas a cada una de las formas estándar.



| Forma                                   | Función                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Región rectangular                      | [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| Región rectangular con esquinas redondeadas | [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Región elíptica                       | [**CreateVelopticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateVelopticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Región poligonal                        | [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Cada función de creación de regiones devuelve un identificador que identifica la nueva región. Una aplicación puede usar este identificador para seleccionar la región en un contexto de dispositivo llamando a la [**función SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) y suministrando este identificador como segundo argumento. Después de seleccionar una región en un contexto de dispositivo, la aplicación puede realizar varias operaciones en ella.

 

 



