---
description: Recupera un rectángulo que representa el área de entrada máxima de la tableta.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: ITablet::GetMaxInputRect (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 422c64a8f5f77b354f02ab9601f7a0c888669d61783afb636816efbdc2e13b27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883545"
---
# <a name="itabletgetmaxinputrect-method"></a>ITablet::GetMaxInputRect (método)

Recupera un rectángulo que representa el área de entrada máxima de la tableta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prcInput* \[ out\]
</dt> <dd>

Puntero al rectángulo que representa el área de entrada máxima de la tableta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITablet (interfaz)**](itablet.md)
</dt> </dl>

 

 




