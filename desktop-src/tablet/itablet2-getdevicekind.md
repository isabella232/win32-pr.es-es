---
description: Devuelve el tipo de dispositivo de hardware que representa el objeto de tableta, como el mouse, el lápiz o la entrada táctil.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'ITablet2:: GetDeviceKind (método)'
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
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720585"
---
# <a name="itablet2getdevicekind-method"></a>ITablet2:: GetDeviceKind (método)

Devuelve el tipo de dispositivo de hardware que representa el objeto de tableta, como el mouse, el lápiz o la entrada táctil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pKind* \[ enuncia\]
</dt> <dd>

Valor de enumeración que indica el tipo de tableta, como el mouse, el lápiz o la entrada táctil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta interfaz y este método se introdujeron en Windows Vista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITablet2**](itablet2.md)
</dt> <dt>

[**\_Enumeración de tipo de dispositivo de tableta \_**](tablet-device-kind.md)
</dt> <dt>

[**Interfaz ITablet**](itablet.md)
</dt> </dl>

 

 




