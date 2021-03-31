---
title: Mensaje EM_GETHYPHENATEINFO (RichEdit. h)
description: Recupera información sobre la división en guiones para un control Rich Edit de Microsoft.
ms.assetid: 70ccb698-e440-493b-8f38-2bf7f32e4b26
keywords:
- EM_GETHYPHENATEINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d083b4bbc4b6854f767395d51dd9899c2a185d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079570"
---
# <a name="em_gethyphenateinfo-message"></a>\_Mensaje GETHYPHENATEINFO em

Recupera información sobre la división en guiones para un control Rich Edit de Microsoft.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estructura [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETHYPHENATEINFO em**](em-sethyphenateinfo.md)
</dt> </dl>

 

 





