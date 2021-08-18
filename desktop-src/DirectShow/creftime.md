---
description: La clase CRefTime es una clase auxiliar para administrar los tiempos de referencia.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: CRefTime (clase, Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d8f9d30b057c1c011dcbff1b7d8c88e9183d50ca1fc2b7dd046b79fe8279d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953964"
---
# <a name="creftime-class"></a>CRefTime (clase)

![jerarquía de clases creftime](images/cutil05.png)

La `CRefTime` clase es una clase auxiliar para administrar los tiempos de referencia.

Un *tiempo de referencia* es una unidad de tiempo representada en unidades de 100 nanosegundos. Esta clase comparte el mismo diseño de datos que el tipo de datos [**REFERENCE \_ TIME,**](reference-time.md) pero agrega algunos métodos y operadores que proporcionan funciones aritméticas, de conversión y de comparación. Para obtener más información sobre las horas de referencia, vea [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).



| Variables de miembro público                                                 | Descripción                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [**m \_ time**](creftime-m-time.md)                                      | Especifica el valor **REFERENCE \_ TIME.**              |
| Métodos públicos                                                          | Descripción                                           |
| [**CRefTime**](creftime-creftime.md)                                   | Método constructor.                                   |
| [**GetUnits**](creftime-getunits.md)                                   | Recupera el tiempo de referencia en unidades de 100 nanosegundos. |
| [**Millisecs**](creftime-millisecs.md)                                 | Convierte el tiempo de referencia en milisegundos.          |
| Operadores                                                               | Descripción                                           |
| [**operador REFERENCE \_ TIME()**](creftime-operator-reference-time-.md) | Convierte el objeto en un tipo **de datos REFERENCE \_ TIME.**  |
| [**operator=**](creftime-operator-assign.md)                           | Asigna una nueva hora de referencia.                         |
| [**operator+=**](creftime-operator-plus-assign.md)                     | Agrega dos tiempos de referencia.                             |
| [**operator =**](creftime-operator-minus-assign.md)                    | Resta una hora de referencia de otra.            |



 

## <a name="remarks"></a>Comentarios

Existe un posible problema con el uso de esta clase. Si aplica el operador += con un objeto **CRefTime** como operando izquierdo y una variable de tipo **LONG** como operando derecho, el compilador coercirá implícitamente el operando derecho en un **objeto CRefTime.** Esta coerción usa el constructor **CRefTime** que convierte milisegundos en unidades DE TIEMPO DE REFERENCIA; como resultado, el operando derecho se multiplica por \_ 10 000:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



Sin embargo, no ocurre lo mismo con el operador + :


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Reftime.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




