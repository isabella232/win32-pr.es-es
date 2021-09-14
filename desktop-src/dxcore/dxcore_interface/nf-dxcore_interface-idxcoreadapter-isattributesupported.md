---
title: IDXCoreAdapter::IsAttributeSupported
description: Determina si este objeto de adaptador DXCore admite el atributo de adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966376"
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

Referencia a un GUID de atributo de adaptador. Para obtener una lista de LOS GUID de atributo, vea GUID de atributos del adaptador [de DXCore.](../dxcore-adapter-attribute-guids.md)

## <a name="returns"></a>Devoluciones

Tipo: **bool**

Devuelve `true` si este objeto de adaptador DXCore admite el atributo de adaptador especificado. De lo contrario, devuelve `false`.

## <a name="see-also"></a>Consulte también

[IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) [REFERENCIA DE DXCore,](../dxcore-reference.md)GUID de atributo de adaptador [dxcore,](../dxcore-adapter-attribute-guids.md) [uso de DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)