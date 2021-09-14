---
title: IDXCoreAdapter::IsPropertySupported
description: Determina si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten la propiedad de adaptador especificada.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966372"
---
# <a name="idxcoreadapterispropertysupported-method"></a>IDXCoreAdapter::IsPropertySupported (método)

Determina si este objeto de adaptador DXCore y el sistema operativo (SO) actual admiten la propiedad de adaptador especificada.

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="property"></a>propiedad

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo de propiedad para la que está consultando sobre la compatibilidad. Consulte la tabla de [DXCoreAdapterProperty para](./ne-dxcore_interface-dxcoreadapterproperty.md) obtener más información sobre cada propiedad del adaptador.

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve si este objeto de adaptador DXCore y el `true` sistema operativo (SO) actual admiten la propiedad de adaptador especificada. De lo contrario, devuelve `false`.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [REFERENCIA DE DXCore,](../dxcore-reference.md)GUID de atributo de adaptador [dxcore,](../dxcore-adapter-attribute-guids.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)