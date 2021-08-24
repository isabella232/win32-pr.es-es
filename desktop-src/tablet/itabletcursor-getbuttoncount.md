---
description: Recupera el número de botones del lápiz óptico de la tableta.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: ITabletCursor::GetButtonCount (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 82a0825d64bc93601b933a98b3a7e0e3f321954d2fb2d7aa285d8d08a315545c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119336025"
---
# <a name="itabletcursorgetbuttoncount-method"></a>ITabletCursor::GetButtonCount (método)

Recupera el número de botones del lápiz óptico de la tableta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcButtons* \[ out\]
</dt> <dd>

Recuento de botones en el lápiz óptico de la tableta.

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
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletCursor (interfaz)**](itabletcursor.md)
</dt> </dl>

 

 




