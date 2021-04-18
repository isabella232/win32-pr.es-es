---
title: Reglas para implementar QueryInterface
description: Reglas para implementar QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705034"
---
# <a name="rules-for-implementing-queryinterface"></a>Reglas para implementar QueryInterface

Hay tres reglas principales que rigen la implementación del método [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) en un objeto com:

-   Los objetos deben tener la identidad.
-   El conjunto de interfaces de una instancia de objeto debe ser estático.
-   Debe ser posible realizar consultas correctamente en cualquier interfaz de un objeto de cualquier otra interfaz.

## <a name="objects-must-have-identity"></a>Los objetos deben tener la identidad

En el caso de una instancia de objeto determinada, una llamada a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) con IID \_ IUnknown siempre debe devolver el mismo valor de puntero físico. Esto le permite llamar a **QueryInterface** en dos interfaces cualesquiera y comparar los resultados para determinar si señalan a la misma instancia de un objeto.

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>El conjunto de interfaces de una instancia de objeto debe ser estático

El conjunto de interfaces accesible en un objeto a través de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) debe ser estático, no dinámico. En concreto, si **QueryInterface** devuelve \_ un valor correcto para un IID determinado una vez, nunca debe devolver e \_ nointerface en llamadas posteriores en el mismo objeto; y si **QueryInterface** devuelve e \_ nointerface para un IID determinado, las llamadas subsiguientes para el mismo IID en el mismo objeto nunca deben devolver S \_ correctos.

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>Debe ser posible realizar consultas correctamente en cualquier interfaz de un objeto de cualquier otra interfaz.

Es decir, según el código siguiente:

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

se aplican las siguientes reglas:

-   Si tiene un puntero a una interfaz en un objeto, se debe realizar una llamada como la siguiente a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para esa misma interfaz:

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   Si una llamada a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para un segundo puntero de interfaz se realiza correctamente, también se debe realizar una llamada a **QueryInterface** desde ese puntero para la primera interfaz. Si se ha obtenido pB correctamente, también se deben realizar las siguientes acciones:

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   Cualquier interfaz debe ser capaz de consultar cualquier otra interfaz en un objeto. Si se ha obtenido pB correctamente y se ha realizado correctamente una consulta para una tercera interfaz (IC) con ese puntero, también debe poder realizar consultas correctamente en el caso de las empresas con el primer puntero, pA. En este caso, la siguiente secuencia debe realizarse correctamente:

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

Las implementaciones de interfaz deben mantener un contador de referencias de puntero pendientes a todas las interfaces de un objeto determinado. Debe utilizar un **entero sin signo** para el contador.

Si un cliente necesita saber que se han liberado recursos, debe usar un método en alguna interfaz en el objeto con una semántica de nivel superior antes de llamar a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar e implementar IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 