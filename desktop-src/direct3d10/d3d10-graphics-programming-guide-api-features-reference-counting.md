---
description: Las funciones set de Direct3D 10 no contienen una referencia a un objeto Device-Child.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Recuento de referencias (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6482918601f163bdea92291eb3927899ca797d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538572"
---
# <a name="reference-counting-direct3d-10"></a><span data-ttu-id="f9be2-103">Recuento de referencias (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f9be2-103">Reference Counting (Direct3D 10)</span></span>

<span data-ttu-id="f9be2-104">Las funciones set de Direct3D 10 no contienen una referencia a un objeto Device-Child.</span><span class="sxs-lookup"><span data-stu-id="f9be2-104">Direct3D 10 set functions do not hold a reference to a device-child object.</span></span> <span data-ttu-id="f9be2-105">Esto significa que cada aplicación debe contener una referencia a un objeto de dispositivo secundario mientras el objeto debe estar enlazado a la canalización.</span><span class="sxs-lookup"><span data-stu-id="f9be2-105">This means that each application must hold a reference to a device-child object for as long as the object needs to be bound to the pipeline.</span></span> <span data-ttu-id="f9be2-106">Cuando el recuento de referencias de un objeto desciende a cero, el objeto se desenlazará de la canalización y se destruirá.</span><span class="sxs-lookup"><span data-stu-id="f9be2-106">When the reference count of an object drops to zero, the object will be unbound from the pipeline and destroyed.</span></span> <span data-ttu-id="f9be2-107">Este estilo de retención de referencia también se conoce como retención de referencia débil porque cada ubicación de enlace de canalización contiene una referencia débil a la interfaz o el objeto que está enlazado a él.</span><span class="sxs-lookup"><span data-stu-id="f9be2-107">This style of reference holding is also known as weak-reference holding because each pipeline binding location holds a weak reference to the interface/object that is bound to it.</span></span>

<span data-ttu-id="f9be2-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f9be2-108">For example:</span></span>


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





|                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9be2-109">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="f9be2-109">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="f9be2-110">En Direct3D 9, las funciones Set contienen una referencia a los objetos de dispositivo. en Direct3D 10, las funciones de conjunto no contienen una referencia a los objetos de dispositivo secundario.</span><span class="sxs-lookup"><span data-stu-id="f9be2-110">In Direct3D 9, set functions hold a reference to the device objects; in Direct3D 10 set functions do not hold a reference to the device-child objects.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f9be2-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9be2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9be2-112">Características de la API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f9be2-112">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




