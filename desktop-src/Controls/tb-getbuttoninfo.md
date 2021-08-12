---
title: TB_GETBUTTONINFO mensaje (Commctrl.h)
description: Recupera información extendida de un botón en una barra de herramientas.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 457b8ca82d570b9d6c55cf97392803fce9a81cbe1d5db8122fcdaa975dd99d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669938"
---
# <a name="tb_getbuttoninfo-message"></a>Mensaje \_ GETBUTTONINFO de TB

Recupera información extendida de un botón en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que recibe la información del botón. Los **miembros cbSize** **y dwMask** de esta estructura deben rellenarse antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero del botón o -1 si se produce un error.

## <a name="remarks"></a>Observaciones

Cuando se usa [**TB \_ ADDBUTTONS**](tb-addbuttons.md) o [**TB \_ INSERTBUTTON**](tb-insertbutton.md) para colocar botones en la barra de herramientas, el texto del botón se especifica normalmente por su índice de grupo de cadenas. **TB \_ GETBUTTONINFO no** recuperará esta cadena. Para usar **TB \_ GETBUTTONINFO para** recuperar el texto del botón, primero debe establecer la cadena de texto con TB [**\_ SETBUTTONINFO**](tb-setbuttoninfo.md). Una vez que haya establecido el texto del botón con **TB \_ SETBUTTONINFO,** ya no puede usar el índice del grupo de cadenas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ GETBUTTONINFOW** (Unicode) y **TB \_ GETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





