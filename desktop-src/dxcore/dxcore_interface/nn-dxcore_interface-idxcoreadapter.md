---
title: IDXCoreAdapter
description: La **interfaz IDXCoreAdapter** implementa métodos para recuperar detalles sobre un elemento de adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 18cdd8082701ea4f1a8b5a3cfa047decd0f77df81b17eebe49bf5a8a887663fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278792"
---
# <a name="idxcoreadapter-interface"></a>Interfaz IDXCoreAdapter

La **interfaz IDXCoreAdapter** implementa métodos para recuperar detalles sobre un elemento de adaptador. **IDXCoreAdapter** hereda de la [interfaz IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown) Para obtener instrucciones de programación y ejemplos de código, vea [Uso de DXCore para enumerar adaptadores.](../dxcore-enum-adapters.md)

## <a name="remarks"></a>Comentarios

Las propiedades de un adaptador se establecen en el momento en que se inicia el adaptador y son inmutables durante la vigencia del adaptador. Esto contrasta con el estado de un adaptador, que se puede consultar o establecer, y cuyos valores pueden cambiar con el tiempo.

## <a name="see-also"></a>Consulte también

[Referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)