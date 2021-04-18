---
title: IDXCoreAdapter::IsPropertySupported
description: Determina si este objeto de adaptador de DXCore y el sistema operativo actual admiten la propiedad de adaptador especificada.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720162"
---
# <a name="idxcoreadapterispropertysupported-method"></a>IDXCoreAdapter:: IsPropertySupported (método)

Determina si este objeto de adaptador de DXCore y el sistema operativo actual admiten la propiedad de adaptador especificada.

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="property"></a>propiedad

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo de propiedad que se va a consultar sobre la compatibilidad con. Vea la tabla en [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) para obtener más información sobre cada propiedad del adaptador.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve  `true`   si este objeto de adaptador de DXCore y el sistema operativo actual admiten la propiedad de adaptador especificada. De lo contrario, devuelve  `false` .

## <a name="see-also"></a>Vea también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore GUID Attribute GUID](../dxcore-adapter-attribute-guids.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)