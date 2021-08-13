---
title: EM_SETHYPHENATEINFO mensaje (Richedit.h)
description: Establece la forma en que un control de edición enriquecido hace la guión.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5551aace3ab054c1c6fa322242ae06386ff19f5a44775bd6dcc6887d19c65c62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437565"
---
# <a name="em_sethyphenateinfo-message"></a>Mensaje \_ EM SETHYPHENATEINFO

Establece la forma en que un control de edición enriquecido hace la guión.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una [**estructura HYPHENATEINFO.**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo)

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa, debe ser cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para habilitar la guión, el cliente debe llamar a [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)y especificar TO \_ ADVANCEDTYPOGRAPHY.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETHYPHENATEINFO**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





