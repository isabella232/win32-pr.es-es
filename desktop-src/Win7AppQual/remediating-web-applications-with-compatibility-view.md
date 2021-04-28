---
description: Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116363"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad

En esta sección se describen los pasos básicos de mitigación y cómo planear la compatibilidad futura de las aplicaciones mientras se abordan los problemas.

Windows Internet Explorer admite los modelos de Internet Explorer heredados siempre que sea factible para que los sitios que desarrolle para ellos sigan comportándose según lo previsto en las versiones más recientes de Internet Explorer. A partir de Windows Internet Explorer 8, puede optar por admitir comportamientos heredados seleccionando el modo de representación en función de la página.

Internet Explorer 8 incluye los siguientes modos de representación que puede establecer mediante el encabezado X-UA-Compatible.



| Valor de content | Descripción                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Use el modo de quirks.                                                                      |
| IE=7          | Use siempre windows Internet Explorer modo 7.                                          |
| IE=EmulateIE7 | Se muestra Internet Explorer modo 7 a menos que el sitio tenga las peculiaridades DOCTYPE.           |
| IE=8          | Use siempre Internet Explorer modo 8.                                                  |
| IE=EmulateIE8 | Invalide Vista de compatibilidad en las máquinas cliente y use Internet Explorer modo 8.      |
| IE=Edge       | Mostrar en el modo más reciente. En Internet Explorer 8, este valor es equivalente a IE=8. |



 

En los temas siguientes se describe cómo actualizar aplicaciones web mediante Vista de compatibilidad.



| Tema                                                                                                  | Descripción                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [¿Qué es Vista de compatibilidad](what-is-compatibility-view-.md)                                          | Describe Vista de compatibilidad.                                                  |
| [¿Por qué necesita Vista de compatibilidad?](why-do-you-need-compatibility-view-.md)                         | Describe por qué debe usar Vista de compatibilidad.                               |
| [Uso de la etiqueta meta para garantizar la compatibilidad futura](use-the-meta-tag-to-ensure-future-compatibility.md) | Describe cómo puede usar el **meta** elemento para garantizar la compatibilidad futura. |



 

 

 



