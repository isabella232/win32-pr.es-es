---
description: Las funciones de conjunto de Direct3D 10 no tienen una referencia a un objeto secundario del dispositivo.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Recuento de referencias (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80745c7af251294dca279a023f541b6485d2c3e01da22d2b8432e7220ac9bbd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793265"
---
# <a name="reference-counting-direct3d-10"></a>Recuento de referencias (Direct3D 10)

Las funciones de conjunto de Direct3D 10 no tienen una referencia a un objeto secundario del dispositivo. Esto significa que cada aplicación debe contener una referencia a un objeto de dispositivo secundario mientras el objeto deba enlazarse a la canalización. Cuando el recuento de referencias de un objeto cae a cero, el objeto se desenlazó de la canalización y se destruirá. Este estilo de retención de referencia también se conoce como retención de referencia débil porque cada ubicación de enlace de canalización contiene una referencia débil a la interfaz o el objeto que está enlazado a ella.

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

- En Direct3D 9, las funciones set tienen una referencia a los objetos del dispositivo; En Direct3D 10, las funciones de conjunto no tienen una referencia a los objetos secundarios del dispositivo.



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




