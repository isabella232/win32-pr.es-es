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
# <a name="reference-counting-direct3d-10"></a>Recuento de referencias (Direct3D 10)

Las funciones set de Direct3D 10 no contienen una referencia a un objeto Device-Child. Esto significa que cada aplicación debe contener una referencia a un objeto de dispositivo secundario mientras el objeto debe estar enlazado a la canalización. Cuando el recuento de referencias de un objeto desciende a cero, el objeto se desenlazará de la canalización y se destruirá. Este estilo de retención de referencia también se conoce como retención de referencia débil porque cada ubicación de enlace de canalización contiene una referencia débil a la interfaz o el objeto que está enlazado a él.

Por ejemplo:


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
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> En Direct3D 9, las funciones Set contienen una referencia a los objetos de dispositivo. en Direct3D 10, las funciones de conjunto no contienen una referencia a los objetos de dispositivo secundario.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de la API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




