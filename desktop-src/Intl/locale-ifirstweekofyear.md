---
description: configuración regional \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "105653119"
---
# <a name="locale_ifirstweekofyear"></a>configuración regional \_ IFIRSTWEEKOFYEAR

La primera semana del año.



| Value | Significado                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | La semana que contiene 1/1 es la primera semana del año. Tenga en cuenta que esto puede ser un solo día, si 1/1 cae el último día de la semana. |
| 1     | La primera semana completa después de 1/1 es la primera semana del año.                                                                     |
| 2     | La primera semana que contiene al menos cuatro días es la primera semana del año. Compatible con ISO 8601.                                     |

Si LOCALE_IFIRSTWEEKOFYEAR es 2, LOCALE_IFIRSTDAYOFWEEK es 0 (lunes) y LOCALE_ICALENDARTYPE es Gregoriana, la primera semana sigue a la definición ISO 8601, donde la primera semana es la semana con el primer jueves del año gregoriano.


 

 

 



