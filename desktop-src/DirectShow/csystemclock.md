---
description: La clase CSystemClock implementa un reloj que devuelve la hora del sistema.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: Clase CSystemClock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104562294"
---
# <a name="csystemclock-class"></a>Clase CSystemClock

![jerarquía de clases csystemclock](images/sclock01.png)

La `CSystemClock` clase implementa un reloj que devuelve la hora del sistema.

Esta clase se deriva de la clase [**CBaseReferenceClock**](cbasereferenceclock.md) y agrega compatibilidad con las interfaces **IPersist** y [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .



| Métodos públicos                                        | Descripción                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [**CreateInstance**](csystemclock-createinstance.md) | Crea una nueva instancia de este objeto.              |
| [**CSystemClock**](csystemclock-csystemclock.md)     | Método de constructor.                                 |
| Métodos IAMClockAdjust                                | Descripción                                         |
| [**SetClockDelta**](csystemclock-setclockdelta.md)   | Ajusta la hora de reloj.                             |
| Métodos IPersist                                      | Descripción                                         |
| [**GetClassID**](csystemclock-getclassid.md)         | Devuelve el identificador de clase (CLSID) del objeto. |



 

 

 



