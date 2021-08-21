---
title: Reglas para implementar QueryInterface
description: Reglas para implementar QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0d0df2d0382c670ed6f4a323f55dcdd1b187430282abe6699da186e574e390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047873"
---
# <a name="rules-for-implementing-queryinterface"></a>Reglas para implementar QueryInterface

Hay tres reglas principales que rigen la implementación del método [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en un objeto COM:

-   Los objetos deben tener identidad.
-   El conjunto de interfaces de una instancia de objeto debe ser estático.
-   Debe ser posible consultar correctamente cualquier interfaz de un objeto desde cualquier otra interfaz.

## <a name="objects-must-have-identity"></a>Los objetos deben tener identidad

Para cualquier instancia de objeto determinada, una llamada a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) con \_ IUnknown IUnknown de IID siempre debe devolver el mismo valor de puntero físico. Esto permite llamar a **QueryInterface en** dos interfaces cualquiera y comparar los resultados para determinar si apuntan a la misma instancia de un objeto.

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>El conjunto de interfaces de una instancia de objeto debe ser estático

El conjunto de interfaces accesibles en un objeto a través de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) debe ser estático, no dinámico. En concreto, si **QueryInterface** devuelve S OK para un IID determinado una vez, nunca debe devolver E NOINTERFACE en las llamadas posteriores en el mismo objeto; y si QueryInterface devuelve E NOINTERFACE para un \_ \_ IID determinado,  las llamadas posteriores para el mismo IID en el mismo objeto nunca deben devolver \_ S \_ OK.

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>Debe ser posible consultar correctamente cualquier interfaz de un objeto desde cualquier otra interfaz.

Es decir, dado el código siguiente:

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

Se aplican las reglas siguientes:

-   Si tiene un puntero a una interfaz en un objeto , una llamada similar a la siguiente a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para esa misma interfaz debe realizarse correctamente:

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   Si una llamada a [**QueryInterface para un**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) segundo puntero de interfaz se realiza correctamente, una llamada a **QueryInterface** desde ese puntero para la primera interfaz también debe realizarse correctamente. Si pB se obtuvo correctamente, lo siguiente también debe realizarse correctamente:

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   Cualquier interfaz debe ser capaz de consultar cualquier otra interfaz en un objeto . Si pB se obtuvo correctamente y se realiza correctamente una consulta para una tercera interfaz (IC) con ese puntero, también debe poder realizar consultas correctamente para IC mediante el primer puntero, pA. En este caso, la secuencia siguiente debe realizarse correctamente:

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

Las implementaciones de interfaz deben mantener un contador de referencias de puntero pendientes a todas las interfaces de un objeto determinado. Debe usar un **entero sin signo para** el contador.

Si un cliente necesita saber que se han liberado los recursos, debe usar un método en alguna interfaz en el objeto con semántica de nivel superior antes de llamar a [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso e implementación de IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 