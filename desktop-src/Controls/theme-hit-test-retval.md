---
title: Valores devueltos de la prueba de posicionamiento
description: En esta sección se enumeran los valores de código de la prueba de posicionamiento que se devuelven en el parámetro pwHitTestCode de la función HitTestThemeBackground.
ms.assetid: 95b4fc1a-2f9b-4464-b672-552d36b60c42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219cb59115bae56ac6cc3ba7f05384c331969b34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075562"
---
# <a name="hit-test-return-values"></a>Valores devueltos de la prueba de posicionamiento

En esta sección se enumeran los valores de código de la prueba de posicionamiento que se devuelven en el parámetro *pwHitTestCode* de la función [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) . Los valores de código devueltos dependen de las opciones de la prueba de posicionamiento especificadas en el parámetro *dwOptions* de la función **HitTestThemeBackground** . Para obtener una lista de las opciones, vea opciones de la [prueba de posicionamiento](theme-hit-test-options.md).

## <a name="return-values"></a>Valores devueltos

En la tabla siguiente se enumeran las opciones de la prueba de posicionamiento y los códigos de retorno correspondientes.



| Opción                       | Códigos de retorno  | Descripción                                                                                                        |
|------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | HTBOTTOM      | La prueba de detección tuvo éxito en el segmento del borde inferior.                                                                   |
|                              | HTBOTTOMLEFT  | La prueba de detección tuvo éxito en la intersección de borde inferior e izquierdo.                                                     |
|                              | HTBOTTOMRIGHT | La prueba de detección tuvo éxito en la intersección de borde inferior y derecho.                                                    |
|                              | HTCLIENT      | La prueba de detección tuvo éxito en el segmento de fondo intermedio.                                                               |
|                              | HTLEFT        | La prueba de detección tuvo éxito en el segmento del borde izquierdo.                                                                     |
|                              | HTNOWHERE     | La prueba de detección tuvo éxito fuera del control o en un área transparente.                                                   |
|                              | HTRIGHT       | La prueba de detección tuvo éxito en el segmento del borde derecho.                                                                    |
|                              | HTTOP         | La prueba de detección tuvo éxito en el segmento del borde superior.                                                                      |
|                              | HTTOPLEFT     | La prueba de detección tuvo éxito en la intersección de borde superior e izquierdo.                                                            |
|                              | HTTOPRIGHT    | La prueba de detección tuvo éxito en la intersección de borde superior y derecho.                                                       |
| \_título HTTB                | HTCAPTION     | La prueba de posicionamiento se realizó correctamente en los segmentos de fondo superior, superior izquierdo o superior derecho.                                         |
|                              | HTNOWHERE     | La prueba de detección tuvo éxito fuera del control o en un área transparente.                                                   |
| HTTB \_ FIXEDBORDER            | HTBORDER      | La prueba de posicionamiento se realizó correctamente en cualquier segmento de fondo excepto en el segmento de fondo intermedio.                                 |
|                              | HTCLIENT      | La prueba de detección tuvo éxito en el segmento de fondo intermedio.                                                               |
| HTTB \_ RESIZINGBORDER         | HTBORDER      | No se pudo realizar la prueba de posicionamiento en el segmento de fondo intermedio y las zonas de cambio de tamaño, pero se realizó correctamente en un segmento de borde de fondo. |
| HTTB \_ RESIZINGBORDER \_ inferior | HTBOTTOM      | La prueba de detección tuvo éxito en el segmento del borde inferior.                                                                   |
| HTTB \_ RESIZINGBORDER \_ izquierda   | HTLEFT        | La prueba de detección tuvo éxito en el segmento del borde izquierdo.                                                                     |
| HTTB \_ RESIZINGBORDER \_ derecha  | HTRIGHT       | La prueba de detección tuvo éxito en el segmento del borde derecho.                                                                    |
| HTTB \_ RESIZINGBORDER \_ superior    | HTTOP         | La prueba de detección tuvo éxito en el segmento del borde superior.                                                                      |



 

 

 




