---
title: Mensaje EM_SETTEXTEX (RichEdit. h)
description: Combina la funcionalidad de los mensajes de WM \_ SETTEXT y em \_ REPLACESEL, y agrega la capacidad de establecer texto mediante una página de códigos y usar texto enriquecido o texto sin formato.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- EM_SETTEXTEX controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491201"
---
# <a name="em_settextex-message"></a>\_Mensaje SETTEXTEX em

Combina la funcionalidad de los mensajes de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) y [**em \_ REPLACESEL**](em-replacesel.md) , y agrega la capacidad de establecer texto mediante una página de códigos y usar texto enriquecido o texto sin formato.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una estructura [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) que especifica las marcas y una página de códigos opcional que se va a usar para traducir a Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al texto terminado en null que se va a insertar. Este texto es una cadena ANSI, a menos que la página de códigos sea 1200 (Unicode). Si *lParam* comienza con una secuencia ASCII RTF válida, por ejemplo, "{ \\ rtf" o "{urtf", el texto se lee mediante el lector RTF.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación está estableciendo todo el texto y se realiza correctamente, el valor devuelto es 1.

Si la operación está estableciendo la selección y se realiza correctamente, el valor devuelto es el número de bytes o caracteres copiados.

Si se produce un error en la operación, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_GETTEXTEX em**](em-gettextex.md)
</dt> <dt>

[**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

