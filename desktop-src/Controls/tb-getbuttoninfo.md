---
title: Mensaje de TB_GETBUTTONINFO (commctrl. h)
description: Recupera información extendida para un botón de una barra de herramientas.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151259"
---
# <a name="tb_getbuttoninfo-message"></a>\_Mensaje GETBUTTONINFO TB

Recupera información extendida para un botón de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que recibe la información del botón. Los miembros **cbSize** y **dwMask** de esta estructura se deben rellenar antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero del botón o-1 si se produce un error.

## <a name="remarks"></a>Observaciones

Al usar [**TB \_ ADDBUTTONS**](tb-addbuttons.md) o [**TB \_ INSERTBUTTON**](tb-insertbutton.md) para colocar botones en la barra de herramientas, el texto del botón se especifica normalmente mediante su índice de grupo de cadenas. **TB \_ GETBUTTONINFO** no recuperará esta cadena. Para usar **TB \_ GETBUTTONINFO** para recuperar el texto del botón, primero debe establecer la cadena de texto con [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md). Una vez que haya establecido el texto del botón con **TB \_ SETBUTTONINFO**, ya no podrá usar el índice del grupo de cadenas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ GETBUTTONINFOW** (Unicode) y **TB \_ GETBUTTONINFOA** (ANSI)<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





