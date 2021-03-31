---
title: Varios niveles de punteros
description: Usar varios niveles de punteros en llamada a procedimiento remoto (RPC).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995472"
---
# <a name="multiple-levels-of-pointers"></a>Varios niveles de punteros

Cuando hay varios niveles de punteros, los atributos se asocian con el puntero más cercano al nombre de la variable. El cliente sigue siendo responsable de asignar cualquier memoria asociada a la respuesta.

En el ejemplo siguiente se permite que el código auxiliar llame al servidor sin conocer de antemano la cantidad de datos que se devolverá:

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

En este ejemplo, el código auxiliar pasa el servidor a un puntero único, que el servidor inicializa en **null**. A continuación, el servidor asigna un bloque de barras, establece el puntero, establece el argumento de tamaño y devuelve. Tenga en cuenta que para que el servidor tenga un efecto en el autor de la llamada, debe pasar un \[ puntero de referencia \] a un \[ puntero [**único**](/windows/desktop/Midl/unique) \] a los datos. Tenga en cuenta también que el tamaño de la coma \[ [**\_ es**](/windows/desktop/Midl/size-is)(, \* pSize) \] , lo que indica que el puntero de nivel superior no es un puntero de tamaño, pero que el puntero de nivel inferior es.

En el lado del cliente, el código auxiliar establece \* ppBar en **null** antes de llamar al procedimiento remoto. A continuación, el código auxiliar asigna y anula la serialización de matriz de los objetos de barra. El argumento de tamaño indica el tamaño del bloque (y el número de barras cuyas referencias no se han calculado). El cliente debe liberar la matriz de objetos de barras devuelta cuando ya no sea necesaria.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**el tamaño \_ es**](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 