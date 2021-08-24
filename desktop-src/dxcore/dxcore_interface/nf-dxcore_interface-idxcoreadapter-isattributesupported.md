---
title: IDXCoreAdapter::IsAttributeSupported
description: Determina si este objeto de adaptador DXCore admite el atributo de adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9dda05ca9dc1d3b7a7a84792c7ac122bb64144d5fdba3ad630be1a3f4d9ddf24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787085"
---
# <a name="idxcoreadapterisattributesupported-method"></a>IDXCoreAdapter::IsAttributeSupported (método)

Determina si este objeto de adaptador DXCore admite el atributo de adaptador especificado.

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="attributeguid"></a>attributeGUID

Tipo: **REFGUID**

Referencia a un GUID de atributo de adaptador. Para obtener una lista de GUID de atributo, vea GUID de atributo del adaptador [de DXCore.](../dxcore-adapter-attribute-guids.md)

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve `true` si este objeto de adaptador DXCore admite el atributo de adaptador especificado. De lo contrario, devuelve `false`.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [DXCore Reference,](../dxcore-reference.md) [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)