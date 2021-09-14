---
title: Varios niveles de punteros
description: Usar varios niveles de punteros en llamada a procedimiento remoto (RPC).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169089"
---
# <a name="multiple-levels-of-pointers"></a>Varios niveles de punteros

Cuando hay varios niveles de punteros, los atributos se asocian al puntero más cercano al nombre de la variable. El cliente sigue siendo responsable de asignar cualquier memoria asociada a la respuesta.

En el ejemplo siguiente se permite que el código auxiliar llame al servidor sin saber de antemano cuántos datos se devolverán:

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

En este ejemplo, el código auxiliar pasa al servidor un puntero único, que el servidor inicializa en **NULL.** A continuación, el servidor asigna un bloque de BAR, establece el puntero, establece el argumento de tamaño y devuelve . Tenga en cuenta que para que el servidor tenga efecto en el autor de la llamada, debe pasar un puntero \[ ref a un puntero único a los \] \[ [](/windows/desktop/Midl/unique) \] datos. Tenga en cuenta también que la coma de tamaño es ( , pSize ), que indica que el puntero de nivel superior no es un puntero de tamaño, pero que el puntero de nivel inferior es \[ [**\_**](/windows/desktop/Midl/size-is) \* \] .

En el lado cliente, el código auxiliar establece \* ppBar en **NULL antes** de llamar al procedimiento remoto. A continuación, el código auxiliar asigna y desmarshals el arrio de objetos BAR. El argumento size indica el tamaño del bloque (y el número de BAR no semarshaled). El cliente debe liberar la matriz devuelta de objetos BAR cuando ya no sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**el \_ tamaño es**](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 