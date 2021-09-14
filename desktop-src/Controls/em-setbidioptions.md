---
title: EM_SETBIDIOPTIONS mensaje (Richedit.h)
description: El mensaje \_ EM SETBIDIOPTIONS establece el estado actual de las opciones bidireccionales en el control de edición enriquecido.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062133"
---
# <a name="em_setbidioptions-message"></a>Mensaje \_ EM SETBIDIOPTIONS

El **mensaje \_ EM SETBIDIOPTIONS** establece el estado actual de las opciones bidireccionales en el control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que indica cómo establecer el estado de las opciones bidireccionales en el control de edición enriquecido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

El control de edición enriquecida debe estar en modo de texto sin formato o **EM \_ SETBIDIOPTIONS** no hará nada.

En los controles de texto sin formato, **EM \_ SETBIDIOPTIONS** determina automáticamente la dirección o alineación del párrafo en función de las reglas de contexto. Estas reglas declaran que la dirección o alineación se deriva del primer carácter fuerte del control. Un carácter seguro es uno a partir del cual se puede determinar la dirección del texto (vea Unicode Standard versión 2.0). La dirección o alineación del párrafo se aplica al formato predeterminado.

**EM \_ SETBIDIOPTIONS solo** cambia el formato de párrafo predeterminado a RTL (de derecha a izquierda) si encuentra un carácter RTL,

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

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ GETBIDIOPTIONS**](em-getbidioptions.md)
</dt> </dl>

 

 





