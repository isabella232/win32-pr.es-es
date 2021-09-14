---
title: EM_SETTEXTEX mensaje (Richedit.h)
description: Combina la funcionalidad de los mensajes WM SETTEXT y \_ EM REPLACESEL, y agrega la capacidad de establecer texto mediante una página de códigos y usar texto enriquecido o \_ texto sin formato.
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
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062058"
---
# <a name="em_settextex-message"></a>Mensaje \_ EM SETTEXTEX

Combina la funcionalidad de los mensajes [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) y [**EM \_ REPLACESEL,**](em-replacesel.md) y agrega la capacidad de establecer texto mediante una página de códigos y usar texto enriquecido o texto sin formato.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una [**estructura SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) que especifica marcas y una página de códigos opcional que se usará para traducir a Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al texto terminado en NULL que se insertará. Este texto es una cadena ANSI, a menos que la página de códigos sea 1200 (Unicode). Si *lParam* comienza con una secuencia RTF ASCII válida, por ejemplo, "{ rtf" o "{urtf", el texto se lee mediante \\ el lector RTF.

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
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETTEXTEX**](em-gettextex.md)
</dt> <dt>

[**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

