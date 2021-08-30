---
title: EM_SETTEXTEX mensaje (Richedit.h)
description: Combina la funcionalidad de los mensajes SETTEXT y EM REPLACESEL de WM, y agrega la capacidad de establecer texto mediante una página de códigos y usar texto enriquecido o \_ \_ texto sin formato.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- EM_SETTEXTEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227e88fc489c274a5c1b194aa79b4b031ad5f0c07bab4110e5b28b3c7cffbf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048045"
---
# <a name="em_settextex-message"></a>Mensaje \_ SETTEXTEX EM

Combina la funcionalidad de los mensajes [**\_ SETTEXT**](/windows/desktop/winmsg/wm-settext) y [**EM \_ REPLACESEL**](em-replacesel.md) de WM, y agrega la capacidad de establecer texto mediante una página de códigos y usar texto enriquecido o texto sin formato.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una [**estructura SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) que especifica marcas y una página de códigos opcional que se usará para traducir a Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al texto terminado en null que se insertará. Este texto es una cadena ANSI, a menos que la página de códigos sea 1200 (Unicode). Si *lParam* comienza con una secuencia ASCII RTF válida, por ejemplo, "{ rtf" o "{urtf", el texto se lee mediante \\ el lector RTF.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación establece todo el texto y se realiza correctamente, el valor devuelto es 1.

Si la operación establece la selección y se realiza correctamente, el valor devuelto es el número de bytes o caracteres copiados.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETTEXTEX**](em-gettextex.md)
</dt> <dt>

[**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

