---
title: VIEW.timerInterval
description: El atributo timerInterval especifica o recupera el intervalo, en milisegundos, en el que el temporizador desenvía eventos al controlador de eventos ontimer.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VIEW.timerInterval Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575621"
---
# <a name="viewtimerinterval"></a>VIEW.timerInterval

El **atributo timerInterval** especifica o recupera el intervalo, en milisegundos, en el que el temporizador desenvía eventos al controlador **de eventos ontimer.**

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de **lectura** y escritura **(long)** con un valor predeterminado de 1000.



| Value        | Descripción                    |
|--------------|--------------------------------|
| 0            | El evento de temporizador no se produce. |
| 50 y posteriores | Intervalo en milisegundos.  |



 

Cualquier valor inferior a 50 (incluidos los números negativos, pero sin incluir cero) genera un error y se mantiene el valor anterior.

## <a name="remarks"></a>Observaciones

Esto no se activa automáticamente si no se implementa ningún controlador de eventos **ontimer.** Por lo tanto, no hay ninguna degradación del rendimiento aunque el valor predeterminado sea distinto de cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> <dt>

[**VIEW.ontimer**](view-ontimer.md)
</dt> </dl>

 

 





