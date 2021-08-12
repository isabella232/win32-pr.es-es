---
title: IDXCoreAdapter::IsQueryStateSupported
description: Determina si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten la consulta del valor del estado del adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8ae77c308cb251982947d91e23eaef8f6d828c1233df442cb013bf9737e3c57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279226"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a>IDXCoreAdapter::IsQueryStateSupported (método)

Determina si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten la consulta del valor del estado del adaptador especificado.

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

El tipo de elemento de estado para el que está consultando sobre la compatibilidad. Consulte la tabla de [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre cada tipo de estado del adaptador.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve si este objeto de adaptador DXCore y el sistema `true` operativo (SO) actual admiten la consulta del estado del adaptador especificado. De lo contrario, devuelve `false`.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [REFERENCIA DE DXCore,](../dxcore-reference.md)GUID de atributo de adaptador [dxcore,](../dxcore-adapter-attribute-guids.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)