---
title: VER. timerInterval
description: El atributo timerInterval especifica o recupera el intervalo, en milisegundos, en el que el temporizador activa eventos al controlador de eventos de tiempo de actividad.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VISTA de Windows Media Player. timerInterval
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718642"
---
# <a name="viewtimerinterval"></a>VER. timerInterval

El atributo **timerInterval** especifica o recupera el intervalo, en milisegundos, en el que el temporizador activa eventos al controlador de eventos de **tiempo de actividad** .

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura y escritura (**Long**) con un valor predeterminado de 1000.



| Value        | Descripción                    |
|--------------|--------------------------------|
| 0            | El evento de temporizador no se activa. |
| 50 y versiones posteriores | Intervalo en milisegundos.  |



 

Cualquier valor por debajo de 50 (incluidos los números negativos, pero sin incluir cero) genera un error y se mantiene el valor anterior.

## <a name="remarks"></a>Observaciones

Esto no se activará automáticamente si no se implementa ningún controlador de eventos de **tiempo de ejecución** . Por lo tanto, no hay degradación del rendimiento, aunque el valor predeterminado sea distinto de cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vista**](view-element.md)
</dt> <dt>

[**VER. tiempo de espera**](view-ontimer.md)
</dt> </dl>

 

 





