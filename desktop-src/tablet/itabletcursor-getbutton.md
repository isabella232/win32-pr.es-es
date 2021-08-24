---
description: Recupera el objeto de botón especificado de un lápiz óptico de tableta.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: ITabletCursor::GetButton (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 49306160a0c14badc23cb2f359400d0fb2947012078a9318315a6697050f48dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938635"
---
# <a name="itabletcursorgetbutton-method"></a>ITabletCursor::GetButton (método)

Recupera el objeto de botón especificado de un lápiz óptico de tableta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iButton* \[ En\]
</dt> <dd>

Identificador del botón que se recuperará.

</dd> <dt>

*ppButton* \[ out\]
</dt> <dd>

Objeto de botón especificado por el *parámetro iButton.*

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

[**ITabletCursor (interfaz)**](itabletcursor.md)
</dt> </dl>

 

 




