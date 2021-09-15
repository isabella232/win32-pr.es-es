---
description: Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566876"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad

En esta sección se describen los pasos básicos de mitigación y cómo planear la compatibilidad futura de las aplicaciones mientras se abordan los problemas.

Windows Internet Explorer admite los modelos de Internet Explorer heredados siempre que sea posible para que los sitios que desarrolle para ellos sigan comportándose según lo previsto en las versiones más recientes de Internet Explorer. A partir Windows Internet Explorer 8, puede optar por admitir comportamientos heredados seleccionando el modo de representación en una página por página.

Internet Explorer 8 incluye los siguientes modos de representación que puede establecer mediante el encabezado compatible con X-UA.



| Valor de content | Descripción                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Use el modo de peculiaridades.                                                                      |
| IE=7          | Use siempre Windows Internet Explorer modo 7.                                          |
| IE=EmulateIE7 | Mostrar en Internet Explorer modo 7 a menos que el sitio tenga las peculiaridades DOCTYPE.           |
| IE=8          | Use siempre Internet Explorer modo 8.                                                  |
| IE=EmulateIE8 | Invalide Vista de compatibilidad en los equipos cliente y use Internet Explorer modo 8.      |
| IE=Edge       | Mostrar en el modo más reciente. En Internet Explorer 8, este valor equivale a IE=8. |



 

En los temas siguientes se describe cómo actualizar aplicaciones web mediante Vista de compatibilidad.



| Tema                                                                                                  | Descripción                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [¿Qué es Vista de compatibilidad](what-is-compatibility-view-.md)                                          | Describe Vista de compatibilidad.                                                  |
| [¿Por qué necesita Vista de compatibilidad?](why-do-you-need-compatibility-view-.md)                         | Describe por qué debe usar Vista de compatibilidad.                               |
| [Uso de la etiqueta meta para garantizar la compatibilidad futura](use-the-meta-tag-to-ensure-future-compatibility.md) | Describe cómo puede usar el **meta** elemento para garantizar la compatibilidad futura. |



 

 

 



