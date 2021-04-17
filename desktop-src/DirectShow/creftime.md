---
description: La clase CRefTime es una clase auxiliar para administrar los tiempos de referencia.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Clase CRefTime (Reftime. h)
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
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660563"
---
# <a name="creftime-class"></a>Clase CRefTime

![jerarquía de clases creftime](images/cutil05.png)

La `CRefTime` clase es una clase auxiliar para administrar los tiempos de referencia.

Una *hora de referencia* es una unidad de tiempo representada en unidades de 100-nanosegundos. Esta clase comparte el mismo diseño de datos que el tipo de datos de [**\_ hora de referencia**](reference-time.md) , pero agrega algunos métodos y operadores que proporcionan funciones aritméticas, de conversión y de comparación. Para obtener más información acerca de los tiempos de referencia, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).



| Variables de miembro público                                                 | Descripción                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [**m \_ hora**](creftime-m-time.md)                                      | Especifica el valor de la **\_ hora de referencia** .              |
| Métodos públicos                                                          | Descripción                                           |
| [**CRefTime**](creftime-creftime.md)                                   | Método de constructor.                                   |
| [**GetUnits**](creftime-getunits.md)                                   | Recupera el tiempo de referencia en unidades de 100-nanosegundos. |
| [**Milisegundos**](creftime-millisecs.md)                                 | Convierte el tiempo de referencia en milisegundos.          |
| Operadores                                                               | Descripción                                           |
| [**tiempo de referencia \_ del operador ()**](creftime-operator-reference-time-.md) | Convierte el objeto en un tipo de datos de **\_ hora de referencia** .  |
| [**operador =**](creftime-operator-assign.md)                           | Asigna una nueva hora de referencia.                         |
| [**operador + =**](creftime-operator-plus-assign.md)                     | Agrega dos tiempos de referencia.                             |
| [**operador =**](creftime-operator-minus-assign.md)                    | Resta una hora de referencia de otra.            |



 

## <a name="remarks"></a>Observaciones

Existe un riesgo potencial con el uso de esta clase. Si aplica el operador + = con un objeto **CRefTime** como operando izquierdo y una variable de tipo **Long** como operando derecho, el compilador convertirá implícitamente el operando derecho en un objeto **CRefTime** . Esta coerción usa el constructor **CRefTime** que convierte los milisegundos en unidades de \_ tiempo de referencia; como resultado, el operando derecho se multiplica por 10.000:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



Sin embargo, no ocurre lo mismo con el operador +:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Reftime. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




