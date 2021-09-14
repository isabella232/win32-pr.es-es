---
title: IDXCoreAdapter::IsSetStateSupported
description: Determina si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten establecer el valor del estado del adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 284e38a622c882fce04278d9134908f55c9a25cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966364"
---
# <a name="idxcoreadapterissetstatesupported-method"></a>IDXCoreAdapter::IsSetStateSupported (método)

Determina si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten establecer el valor del estado del adaptador especificado.

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

El tipo de elemento de estado para el que está consultando sobre la compatibilidad. Consulte la tabla de [DXCoreAdapterState para](./ne-dxcore_interface-dxcoreadapterstate.md) obtener más información sobre cada tipo de estado del adaptador.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten la `true` configuración del estado del adaptador especificado. De lo contrario, devuelve `false`.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [REFERENCIA DE DXCore,](../dxcore-reference.md)GUID de atributo de adaptador [dxcore,](../dxcore-adapter-attribute-guids.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)