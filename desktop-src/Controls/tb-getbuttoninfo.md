---
title: TB_GETBUTTONINFO mensaje (Commctrl.h)
description: Recupera información extendida para un botón de una barra de herramientas.
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
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166850"
---
# <a name="tb_getbuttoninfo-message"></a>Mensaje \_ GETBUTTONINFO de TB

Recupera información extendida para un botón de una barra de herramientas.

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

Cuando se usa [**TB \_ ADDBUTTONS**](tb-addbuttons.md) o [**TB \_ INSERTBUTTON**](tb-insertbutton.md) para colocar botones en la barra de herramientas, el texto del botón se especifica normalmente por su índice de grupo de cadenas. **TB \_ GETBUTTONINFO** no recuperará esta cadena. Para usar **TB \_ GETBUTTONINFO para** recuperar texto de botón, primero debe establecer la cadena de texto con TB [**\_ SETBUTTONINFO**](tb-setbuttoninfo.md). Una vez que haya establecido el texto del botón **con TB \_ SETBUTTONINFO,** ya no podrá usar el índice del grupo de cadenas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ GETBUTTONINFOW** (Unicode) y **TB \_ GETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





