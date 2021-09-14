---
title: Valores devueltos de la prueba de impacto
description: En esta sección se enumeran los valores de código de prueba de acceso que se devuelven en el parámetro pwHitTestCode de la función HitTestThemeBackground.
ms.assetid: 95b4fc1a-2f9b-4464-b672-552d36b60c42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219cb59115bae56ac6cc3ba7f05384c331969b34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166046"
---
# <a name="hit-test-return-values"></a>Valores devueltos de la prueba de impacto

En esta sección se enumeran los valores de código de prueba de acceso que se devuelven en el parámetro *pwHitTestCode* de la [**función HitTestThemeBackground.**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) Los valores de código devueltos dependen de las opciones de la prueba de acceso especificadas en el *parámetro dwOptions* de la **función HitTestThemeBackground.** Para obtener una lista de las opciones, vea [Hit Test Options](theme-hit-test-options.md).

## <a name="return-values"></a>Valores devueltos

En la tabla siguiente se enumeran las opciones de prueba de acceso y los códigos de retorno correspondientes.



| Opción                       | Códigos de retorno  | Descripción                                                                                                        |
|------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | HTBOTTOM      | La prueba de pulsación se ha alcanzado correctamente en el segmento del borde inferior.                                                                   |
|                              | HTBOTTOMLEFT  | La prueba de pulsación se ha alcanzado correctamente en la intersección del borde inferior e izquierdo.                                                     |
|                              | HTBOTTOMRIGHT | La prueba de pulsación se ha correcto en la intersección del borde inferior y derecho.                                                    |
|                              | HTCLIENT      | La prueba de éxito se ha logrado en el segmento central del fondo.                                                               |
|                              | HTLEFT        | La prueba de pulsación se ha alcanzado correctamente en el segmento del borde izquierdo.                                                                     |
|                              | HTNOWHERE     | La prueba de acceso se ha alcanzado correctamente fuera del control o en un área transparente.                                                   |
|                              | HTRIGHT       | La prueba de pulsación se ha correcto en el segmento del borde derecho.                                                                    |
|                              | HTTOP         | La prueba de selección se ha alcanzado correctamente en el segmento de borde superior.                                                                      |
|                              | HTTOPLEFT     | La prueba de selección se ha alcanzado correctamente en la intersección de borde superior e izquierdo.                                                            |
|                              | HTTOPRIGHT    | La prueba de selección se ha alcanzado correctamente en la intersección del borde superior y derecho.                                                       |
| TÍTULO DE \_ HTTB                | HOTELAPTION     | La prueba de selección se ha hecho correctamente en los segmentos de fondo superior, superior izquierda o superior derecha.                                         |
|                              | HTNOWHERE     | La prueba de acceso se ha alcanzado correctamente fuera del control o en un área transparente.                                                   |
| HTTB \_ FIXEDBORDER            | HTBORDER      | La prueba de impacto se ha hecho correctamente en cualquier segmento de fondo, excepto en el segmento de fondo central.                                 |
|                              | HTCLIENT      | La prueba de éxito se ha logrado en el segmento central del fondo.                                                               |
| HTTB \_ RESIZINGBORDER         | HTBORDER      | No se pudo realizar la prueba de impacto en el segmento de fondo central y se han redimensionado las zonas, pero se ha podido realizar correctamente en un segmento de borde de fondo. |
| HTTB \_ RESIZINGBORDER \_ BOTTOM | HTBOTTOM      | La prueba de pulsación se ha alcanzado correctamente en el segmento del borde inferior.                                                                   |
| HTTB \_ RESIZINGBORDER \_ LEFT   | HTLEFT        | La prueba de pulsación se ha alcanzado correctamente en el segmento del borde izquierdo.                                                                     |
| DERECHO DE \_ RESIZINGBORDER HTTB \_  | HTRIGHT       | La prueba de pulsación se ha correcto en el segmento del borde derecho.                                                                    |
| HTTB \_ RESIZINGBORDER \_ TOP    | HTTOP         | La prueba de selección se ha alcanzado correctamente en el segmento de borde superior.                                                                      |



 

 

 




