---
title: IDXCoreAdapter::IsSetStateSupported
description: Determina si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten la configuración del valor del estado del adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: dc63b541a552f1b01792e9f503acc7aeee03ce5ac6cc92e7b70e271ae62a50ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278983"
---
# <a name="idxcoreadapterissetstatesupported-method"></a>IDXCoreAdapter::IsSetStateSupported (método)

Determina si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten la configuración del valor del estado del adaptador especificado.

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Tipo de elemento de estado para el que se consulta la compatibilidad. Consulte la tabla de [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre cada tipo de estado del adaptador.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten la configuración `true` del estado del adaptador especificado. De lo contrario, devuelve `false`.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [DXCore Reference,](../dxcore-reference.md) [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)