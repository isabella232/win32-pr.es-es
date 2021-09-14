---
description: La clase COARefTime convierte los tiempos de referencia entre segundos y unidades de 100 nanosegundos.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Clase COARefTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070077"
---
# <a name="coareftime-class"></a>COARefTime (clase)

![jerarquía de clases coareftime](images/cutil05.png)

La `COARefTime` clase convierte los tiempos de referencia entre segundos y unidades de 100 nanosegundos.

Esta clase convierte entre los tiempos de referencia que son compatibles con Automation y los tiempos de referencia que son compatibles con C/C++. Las interfaces compatibles con Automation usan **valores double** para representar el tiempo en segundos. Otras interfaces usan valores **LONGLONG** de 64 bits para representar el tiempo en unidades de 100 nanosegundos. Los siguientes tipos se definen para estos valores:

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

Los filtros pueden usar la `COARefTime` clase para convertir entre los dos formatos. Esta clase se deriva de la [**clase CRefTime.**](creftime.md)



| Métodos públicos                                          | Descripción                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [**COARefTime**](coareftime-coareftime.md)             | Método constructor.                                                   |
| Operadores                                               | Descripción                                                           |
| [**double**](coareftime-double.md)                     | Convierte la hora de referencia en un **valor** double.                    |
| [**TIEMPO DE \_ REFERENCIA**](coareftime-reference-time.md)    | Convierte el objeto en un **valor REFERENCE \_ TIME.**                      |
| [**operator =**](coareftime-operator-assign.md)        | Asigna una nueva hora de referencia.                                         |
| [**operator ==**](coareftime-operator-eq.md)           | Comprueba la igualdad entre dos tiempos de referencia.                       |
| [**operador !=**](cmediatype-operator-neq.md)          | Comprueba si hay desigualdad entre dos tiempos de referencia.                     |
| [**operador <**](coareftime-operator-lt.md)         | Comprueba si una hora de referencia es menor que otra.                     |
| [**operador >**](coareftime-operator-gt.md)         | Comprueba si una hora de referencia es mayor que otra.                  |
| [**operator <=**](coareftime-operator-lteq.md)      | Comprueba si una hora de referencia es menor o igual que otra.         |
| [**operator >=**](coareftime-operator-gteq.md)      | Comprueba si una hora de referencia es mayor o igual que otra.      |
| [**operador +**](coareftime-operator-plus.md)          | Agrega dos tiempos de referencia.                                             |
| [**operador **](coareftime-operator-minus.md)         | Resta una hora de referencia de otra.                            |
| [**operador +=**](coareftime-operator-plus-assign.md)  | Agrega dos tiempos de referencia y asigna el resultado a este objeto .      |
| [**operator =**](coareftime-operator-minus-assign.md) | Resta dos veces la referencia y asigna el resultado a este objeto. |
| [**Operador \***](coareftime-operator-mult.md)         | Multiplica un tiempo de referencia por un valor.                               |
| [**operador /**](coareftime-operator-div.md)           | Divide un tiempo de referencia por un valor.                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




