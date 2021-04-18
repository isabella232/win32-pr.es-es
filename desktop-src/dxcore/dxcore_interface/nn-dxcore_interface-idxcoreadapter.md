---
title: IDXCoreAdapter
description: La interfaz **IDXCoreAdapter**   implementa métodos para recuperar detalles sobre un elemento de adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149550"
---
# <a name="idxcoreadapter-interface"></a>Interfaz IDXCoreAdapter

La interfaz **IDXCoreAdapter**   implementa métodos para recuperar detalles sobre un elemento de adaptador. **IDXCoreAdapter** hereda de la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).

## <a name="remarks"></a>Observaciones

Las propiedades de un adaptador se establecen en el momento en que se inicia el adaptador y son inmutables mientras dure el adaptador. Esto contrasta con el estado de un adaptador, que se puede consultar o establecer, y los valores de que pueden cambiar con el tiempo.

## <a name="see-also"></a>Vea también

[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)