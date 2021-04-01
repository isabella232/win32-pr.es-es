---
title: Mensaje EM_SETHYPHENATEINFO (RichEdit. h)
description: Establece la forma en que un control Rich Edit realiza la división en guiones.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905522"
---
# <a name="em_sethyphenateinfo-message"></a>\_Mensaje SETHYPHENATEINFO em

Establece la forma en que un control Rich Edit realiza la división en guiones.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una estructura [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza, debe ser cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para habilitar la división de palabras, el cliente debe llamar a [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), especificando a \_ ADVANCEDTYPOGRAPHY.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETHYPHENATEINFO em**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





