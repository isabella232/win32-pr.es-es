---
description: Devuelve el tipo de dispositivo de hardware que el objeto de tableta representa, como el mouse, el lápiz o la entrada táctil.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: ITablet2::GetDeviceKind (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e1db540b1097428e20104d95a8a7a6726566c7cd8939a11ec4041c1aa9475afd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450532"
---
# <a name="itablet2getdevicekind-method"></a>ITablet2::GetDeviceKind (método)

Devuelve el tipo de dispositivo de hardware que el objeto de tableta representa, como el mouse, el lápiz o la entrada táctil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pKind* \[ out\]
</dt> <dd>

Valor de enumeración que indica el tipo de tableta, como mouse, lápiz o toque.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta interfaz y método se introdujeron en Windows Vista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITablet2 (interfaz)**](itablet2.md)
</dt> <dt>

[**Enumeración TABLET \_ DEVICE \_ KIND**](tablet-device-kind.md)
</dt> <dt>

[**ITablet (interfaz)**](itablet.md)
</dt> </dl>

 

 




