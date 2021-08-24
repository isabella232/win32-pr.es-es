---
title: IDXCoreAdapter::IsValid
description: Determina si este objeto de adaptador DXCore sigue siendo válido.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6b8a0ccadb46f20db9c5f2a23ac8709b391254ee453f05424dadee309f33fc40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842545"
---
# <a name="idxcoreadapterisvalid-method"></a>IDXCoreAdapter::IsValid (método)

Determina si este objeto de adaptador DXCore sigue siendo válido. Para obtener instrucciones de programación y ejemplos de código, [vea Uso de DXCore para enumerar adaptadores.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve `true` si este objeto de adaptador DXCore sigue siendo válido. De lo contrario, devuelve `false`.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [referencia de DXCore,](../dxcore-reference.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)