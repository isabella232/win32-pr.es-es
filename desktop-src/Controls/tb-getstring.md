---
title: TB_GETSTRING mensaje (Commctrl.h)
description: Recupera una cadena del grupo de cadenas de una barra de herramientas.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- TB_GETSTRING controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d25cbf20fd084c2ce60b29d131b7f488ca2b8cee178a2218fcfac191b3c1af33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918495"
---
# <a name="tb_getstring-message"></a>Mensaje \_ GETSTRING de TB

Recupera una cadena del grupo de cadenas de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la longitud del búfer *lParam,* en bytes. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el índice de la cadena.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer utilizado para devolver la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la longitud de cadena si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Comentarios

Este mensaje devuelve la cadena especificada del grupo de cadenas de la barra de herramientas. No se corresponde necesariamente con la cadena de texto que se muestra actualmente mediante un botón. Para recuperar la cadena de texto actual de un botón, envíe a la barra de herramientas [**un mensaje \_ GETBUTTONTEXT de TB.**](tb-getbuttontext.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ GETSTRINGW** (Unicode) y **TB \_ GETSTRINGA** (ANSI)<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TB \_ ADDSTRING**](tb-addstring.md)
</dt> <dt>

[**TB \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

