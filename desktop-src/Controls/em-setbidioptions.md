---
title: Mensaje EM_SETBIDIOPTIONS (RichEdit. h)
description: El \_ mensaje SETBIDIOPTIONS em establece el estado actual de las opciones bidireccionales en el control Rich Edit.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150923"
---
# <a name="em_setbidioptions-message"></a>\_Mensaje SETBIDIOPTIONS em

El **mensaje \_ SETBIDIOPTIONS em** establece el estado actual de las opciones bidireccionales en el control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que indica cómo establecer el estado de las opciones bidireccionales en el control Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El control Rich Edit debe estar en modo de texto sin formato o **em \_ SETBIDIOPTIONS** no hará nada.

En los controles de texto sin formato, **em \_ SETBIDIOPTIONS** determina automáticamente la dirección del párrafo y/o la alineación en función de las reglas de contexto. Estas reglas determinan que la dirección y/o la alineación se derivan del primer carácter fuerte del control. Un carácter seguro es aquél del que se puede determinar la dirección del texto (vea la versión 2,0 del estándar Unicode). La dirección del párrafo y/o la alineación se aplican al formato predeterminado.

**Em \_ SETBIDIOPTIONS** solo cambia el formato de párrafo predeterminado a RTL (de derecha a izquierda) si encuentra un carácter RTL,

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

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**\_GETBIDIOPTIONS em**](em-getbidioptions.md)
</dt> </dl>

 

 





