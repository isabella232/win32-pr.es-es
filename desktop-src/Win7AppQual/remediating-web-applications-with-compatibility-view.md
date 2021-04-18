---
description: .
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43f4ff54a919058127a5f72ba60f3683c6583e1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717363"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad

En esta sección se describen los pasos básicos de mitigación y cómo planear la compatibilidad con aplicaciones futuras mientras se abordan los problemas ahora.

Windows Internet Explorer es compatible con los modelos heredados de Internet Explorer siempre que sea factible para que los sitios que desarrolle en ellos sigan comportándose de la manera esperada en las versiones más recientes de Internet Explorer. A partir de Windows Internet Explorer 8, puede elegir admitir comportamientos heredados seleccionando el modo de representación página por página.

Internet Explorer 8 incluye los siguientes modos de representación que se pueden establecer mediante el encabezado X-UA-compatible.



| Valor de content | Descripción                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Usar el modo no estándar.                                                                      |
| IE = 7          | Use siempre el modo de Windows Internet Explorer 7.                                          |
| IE=EmulateIE7 | Mostrar en modo Internet Explorer 7 a menos que el sitio tenga el DOCTYPE no estándar.           |
| IE = 8          | Use siempre el modo Internet Explorer 8.                                                  |
| IE=EmulateIE8 | Invalide la vista de compatibilidad en los equipos cliente y use el modo Internet Explorer 8.      |
| IE=Edge       | Mostrar en el modo más reciente. En Internet Explorer 8, este valor es equivalente a IE = 8. |



 

En los temas siguientes se describe cómo actualizar aplicaciones web mediante la vista de compatibilidad.



| Tema                                                                                                  | Descripción                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Qué es la vista de compatibilidad](what-is-compatibility-view-.md)                                          | Describe la vista de compatibilidad.                                                  |
| [¿Por qué necesita la vista de compatibilidad?](why-do-you-need-compatibility-view-.md)                         | Describe por qué debe usar la vista de compatibilidad.                               |
| [Usar la etiqueta meta para garantizar compatibilidad futura](use-the-meta-tag-to-ensure-future-compatibility.md) | Describe cómo se puede usar el elemento **meta** para garantizar la compatibilidad futura. |



 

 

 



