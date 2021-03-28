---
description: Una aplicación crea una región mediante una llamada a una función asociada a una forma específica. En la tabla siguiente se muestran las funciones asociadas a cada una de las formas estándar.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Creación y selección de regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984835"
---
# <a name="region-creation-and-selection"></a>Creación y selección de regiones

Una aplicación crea una región mediante una llamada a una función asociada a una forma específica. En la tabla siguiente se muestran las funciones asociadas a cada una de las formas estándar.



| Forma                                   | Función                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Región rectangular                      | [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| Región rectangular con esquinas redondeadas | [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Región elíptica                       | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Región poligonal                        | [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Cada función de creación de regiones devuelve un identificador que identifica la nueva región. Una aplicación puede usar este identificador para seleccionar la región en un contexto de dispositivo llamando a la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) y proporcionando este identificador como segundo argumento. Después de seleccionar una región en un contexto de dispositivo, la aplicación puede realizar varias operaciones en ella.

 

 



