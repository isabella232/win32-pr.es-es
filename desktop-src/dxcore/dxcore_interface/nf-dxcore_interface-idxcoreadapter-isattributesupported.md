---
title: IDXCoreAdapter::IsAttributeSupported
description: Determina si este objeto de adaptador DXCore admite el atributo de adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420858"
---
# <a name="idxcoreadapterisattributesupported-method"></a>IDXCoreAdapter:: IsAttributeSupported (método)

Determina si este objeto de adaptador DXCore admite el atributo de adaptador especificado.

## <a name="syntax"></a>Sintaxis

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>Parámetros

### <a name="attributeguid"></a>attributeGUID

Tipo: **REFGUID**

Referencia a un GUID de atributo de adaptador. Para obtener una lista de los GUID de atributo, consulte [GUID del atributo del adaptador de DXCore](../dxcore-adapter-attribute-guids.md).

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve  `true`   si este objeto de adaptador de DXCore admite el atributo de adaptador especificado. De lo contrario, devuelve  `false` .

## <a name="see-also"></a>Vea también

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore GUID Attribute GUID](../dxcore-adapter-attribute-guids.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)