---
description: Recupera el identificador del lápiz óptico.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: ITabletCursor::GetId (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a7dc053b880c3ebaf4b94ae88a09c85f32f1dd5b8dc335756c8906c9a6f0fb4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938625"
---
# <a name="itabletcursorgetid-method"></a>ITabletCursor::GetId (método)

Recupera el identificador del lápiz óptico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCid* \[ out\]
</dt> <dd>

Identificador del lápiz óptico de tableta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

CURSOR \_ ID se define como DWORD.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletCursor (interfaz)**](itabletcursor.md)
</dt> </dl>

 

 




