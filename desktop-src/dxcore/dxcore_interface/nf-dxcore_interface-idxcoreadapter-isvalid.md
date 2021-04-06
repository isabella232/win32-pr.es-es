---
title: IDXCoreAdapter::IsValid
description: Determina si este objeto de adaptador DXCore sigue siendo válido.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f58d8607b75253efda2e111eb358f576d36b65f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078130"
---
# <a name="idxcoreadapterisvalid-method"></a>IDXCoreAdapter:: IsValid (método)

Determina si este objeto de adaptador DXCore sigue siendo válido. Para obtener instrucciones de programación y ejemplos de código, vea [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve  `true`   si este objeto de adaptador de DXCore sigue siendo válido. De lo contrario, devuelve  `false` .

## <a name="see-also"></a>Vea también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)