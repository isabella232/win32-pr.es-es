---
title: EM_GETTEXTMODE mensaje (Richedit.h)
description: Obtiene el modo de texto actual y el nivel de deshacer de un control de edición enriquecido.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- EM_GETTEXTMODE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb790a05920cd065e5b8c7fe97bc3d9539ae5ea2b75277f4bfe3c6dabbd8ebe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048775"
---
# <a name="em_gettextmode-message"></a>Mensaje \_ EM GETTEXTMODE

Obtiene el modo de texto actual y el nivel de deshacer de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno o varios valores del tipo de [**enumeración TEXTMODE.**](/windows/win32/api/richedit/ne-richedit-textmode) Los valores indican el modo de texto actual y el nivel de deshacer del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETTEXTMODE**](em-settextmode.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





