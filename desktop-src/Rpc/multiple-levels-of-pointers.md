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
# <a name="multiple-levels-of-pointers"></a><span data-ttu-id="eaf05-103">Varios niveles de punteros</span><span class="sxs-lookup"><span data-stu-id="eaf05-103">Multiple Levels of Pointers</span></span>

<span data-ttu-id="eaf05-104">Cuando hay varios niveles de punteros, los atributos se asocian con el puntero más cercano al nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="eaf05-104">When there are multiple levels of pointers, the attributes are associated with the pointer closest to the variable name.</span></span> <span data-ttu-id="eaf05-105">El cliente sigue siendo responsable de asignar cualquier memoria asociada a la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eaf05-105">The client is still responsible for allocating any memory associated with the response.</span></span>

<span data-ttu-id="eaf05-106">En el ejemplo siguiente se permite que el código auxiliar llame al servidor sin conocer de antemano la cantidad de datos que se devolverá:</span><span class="sxs-lookup"><span data-stu-id="eaf05-106">The following example allows the stub to call the server without knowing in advance how much data will be returned:</span></span>

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

<span data-ttu-id="eaf05-107">En este ejemplo, el código auxiliar pasa el servidor a un puntero único, que el servidor inicializa en **null**.</span><span class="sxs-lookup"><span data-stu-id="eaf05-107">In this example, the stub passes the server a unique pointer, which the server initializes to **NULL**.</span></span> <span data-ttu-id="eaf05-108">A continuación, el servidor asigna un bloque de barras, establece el puntero, establece el argumento de tamaño y devuelve.</span><span class="sxs-lookup"><span data-stu-id="eaf05-108">The server then allocates a block of BARs, sets the pointer, sets the size argument and returns.</span></span> <span data-ttu-id="eaf05-109">Tenga en cuenta que para que el servidor tenga un efecto en el autor de la llamada, debe pasar un \[ puntero de referencia \] a un \[ puntero [**único**](/windows/desktop/Midl/unique) \] a los datos.</span><span class="sxs-lookup"><span data-stu-id="eaf05-109">Note that in order for the server to have an effect on the caller you must pass a \[ref\] pointer to a \[[**unique**](/windows/desktop/Midl/unique)\] pointer to your data.</span></span> <span data-ttu-id="eaf05-110">Tenga en cuenta también que el tamaño de la coma \[ [**\_ es**](/windows/desktop/Midl/size-is)(, \* pSize) \] , lo que indica que el puntero de nivel superior no es un puntero de tamaño, pero que el puntero de nivel inferior es.</span><span class="sxs-lookup"><span data-stu-id="eaf05-110">Also note the comma in \[[**size\_is**](/windows/desktop/Midl/size-is)( , \*pSize )\], which indicates that the top-level pointer is not a sized pointer, but that the lower-level pointer is.</span></span>

<span data-ttu-id="eaf05-111">En el lado del cliente, el código auxiliar establece \* ppBar en **null** antes de llamar al procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="eaf05-111">On the client side, the stub sets \*ppBar to **NULL** before calling the remote procedure.</span></span> <span data-ttu-id="eaf05-112">A continuación, el código auxiliar asigna y anula la serialización de matriz de los objetos de barra.</span><span class="sxs-lookup"><span data-stu-id="eaf05-112">The stub then allocates and unmarshals the arry of BAR objects.</span></span> <span data-ttu-id="eaf05-113">El argumento de tamaño indica el tamaño del bloque (y el número de barras cuyas referencias no se han calculado).</span><span class="sxs-lookup"><span data-stu-id="eaf05-113">The size argument indicates the size of the block (and the number of unmarshaled BARs).</span></span> <span data-ttu-id="eaf05-114">El cliente debe liberar la matriz de objetos de barras devuelta cuando ya no sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="eaf05-114">The client must free the returned array of BAR objects when it is no longer required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaf05-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eaf05-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaf05-116">**el tamaño \_ es**</span><span class="sxs-lookup"><span data-stu-id="eaf05-116">**size\_is**</span></span>](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 