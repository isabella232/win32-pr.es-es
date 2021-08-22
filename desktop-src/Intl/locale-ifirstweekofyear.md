---
description: CONFIGURACIÓN REGIONAL \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: da0d8697e8a02bb6943f4a4154a1ea89c4e01cbaed7576631e3a61d161e80503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147428"
---
# <a name="locale_ifirstweekofyear"></a>CONFIGURACIÓN REGIONAL \_ IFIRSTWEEKOFYEAR

La primera semana del año.



| Value | Significado                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | La semana que contiene 1/1 es la primera semana del año. Tenga en cuenta que puede ser un solo día, si 1/1 cae en el último día de la semana. |
| 1     | La primera semana completa después del 1/1 es la primera semana del año.                                                                     |
| 2     | La primera semana que contiene al menos cuatro días es la primera semana del año. Compatible con ISO 8601.                                     |

Si LOCALE_IFIRSTWEEKOFYEAR es 2, LOCALE_IFIRSTDAYOFWEEK es 0 (lunes) y LOCALE_ICALENDARTYPE es gregoriano, la primera semana sigue la definición iso 8601, donde la primera semana es la semana con el primer jueves del año gregoriano.


 

 

 



