---
description: Las funciones de conjunto de Direct3D 10 no tienen una referencia a un objeto de dispositivo secundario.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Recuento de referencias (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3587466aa3ecaea5f3a77332c77654b0725bb1
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335459"
---
# <a name="reference-counting-direct3d-10"></a>Recuento de referencias (Direct3D 10)

Las funciones de conjunto de Direct3D 10 no tienen una referencia a un objeto de dispositivo secundario. Esto significa que cada aplicación debe contener una referencia a un objeto de dispositivo secundario mientras el objeto deba enlazarse a la canalización. Cuando el recuento de referencias de un objeto cae a cero, el objeto se desenlazó de la canalización y se destruirá. Este estilo de retención de referencia también se conoce como retención de referencia débil porque cada ubicación de enlace de canalización contiene una referencia débil a la interfaz o el objeto que está enlazado a ella.

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





Diferencias entre Direct3D 9 y Direct3D 10:

- En Direct3D 9, las funciones set tienen una referencia a los objetos del dispositivo; En Las funciones de conjunto de Direct3D 10 no tienen una referencia a los objetos secundarios del dispositivo.



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




