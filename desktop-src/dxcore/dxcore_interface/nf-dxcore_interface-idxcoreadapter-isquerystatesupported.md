---
title: IDXCoreAdapter::IsQueryStateSupported
description: Determina si este objeto de adaptador de DXCore y el sistema operativo actual admiten la consulta del valor del estado del adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d154597f9b3ddbec24cff230317d881b9595bcde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149474"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a>IDXCoreAdapter:: IsQueryStateSupported (método)

Determina si este objeto de adaptador de DXCore y el sistema operativo actual admiten la consulta del valor del estado del adaptador especificado.

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

El tipo de elemento de estado que está consultando sobre la compatibilidad con. Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cada tipo de estado del adaptador.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve  `true`   si este objeto de adaptador de DXCore y el sistema operativo actual admiten consultas en el estado del adaptador especificado. De lo contrario, devuelve  `false` .

## <a name="see-also"></a>Vea también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore GUID Attribute GUID](../dxcore-adapter-attribute-guids.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)