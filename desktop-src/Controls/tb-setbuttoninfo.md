---
title: TB_SETBUTTONINFO mensaje (Commctrl.h)
description: Establece la información de un botón existente en una barra de herramientas.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- TB_SETBUTTONINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e9fa1da0f9556c025b83ac2b3345680fe11dac0dd15e202ed7336cacfe511e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829629"
---
# <a name="tb_setbuttoninfo-message"></a>Mensaje \_ SETBUTTONINFO de TB

Establece la información de un botón existente en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de botón.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que contiene la nueva información del botón. Los **miembros cbSize** **y dwMask** de esta estructura deben rellenarse antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

El texto se asigna normalmente a los botones cuando se agregan a una barra de herramientas especificando el índice de una cadena en el grupo de cadenas de la barra de herramientas. Si usa un **\_ ELEMENTO SETBUTTONINFO de TB** para asignar texto nuevo a un botón, invalidará permanentemente el texto del grupo de cadenas. Puede cambiar el texto llamando de nuevo **a TB \_ SETBUTTONINFO,** pero no puede reasignar la cadena del grupo de cadenas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ SETBUTTONINFOW** (Unicode) y **TB \_ SETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TB \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> <dt>

[**TB \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

 





