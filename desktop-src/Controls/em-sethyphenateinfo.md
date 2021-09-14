---
title: EM_SETHYPHENATEINFO (Richedit.h)
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
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062100"
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
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETHYPHENATEINFO**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





