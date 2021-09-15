---
description: Extiende la interfaz ITablet.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Interfaz ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579469"
---
# <a name="itablet2-interface"></a>Interfaz ITablet2

Extiende la [**interfaz ITablet**](itablet.md).

## <a name="members"></a>Members

La **interfaz ITablet2** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITablet2 también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITablet2** tiene estos métodos.



| Método                                          | Descripción                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**GetDeviceKind**](itablet2-getdevicekind.md) | Devuelve el tipo de dispositivo de hardware que el objeto de tableta representa, como el mouse, el lápiz o la entrada táctil.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta interfaz se introdujo en Windows Vista.

Los desarrolladores no deben usar esta interfaz.

En el código siguiente se describe cómo se define la interfaz **ITablet2.**

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

