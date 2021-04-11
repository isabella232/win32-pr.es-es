---
title: Mensaje de TB_GETSTRING (commctrl. h)
description: Recupera una cadena del grupo de cadenas de una barra de herramientas.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- TB_GETSTRING controles de mensajes de Windows
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
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079129"
---
# <a name="tb_getstring-message"></a>TB \_ mensaje de GETSTRING

Recupera una cadena del grupo de cadenas de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la longitud del búfer *lParam* , en bytes. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el índice de la cadena.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que se usa para devolver la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la longitud de la cadena si se realiza correctamente, o-1 en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje devuelve la cadena especificada del grupo de cadenas de la barra de herramientas. No se corresponde necesariamente con la cadena de texto que se muestra actualmente en un botón. Para recuperar la cadena de texto actual de un botón, envíe la barra de herramientas a un mensaje [**\_ GETBUTTONTEXT TB**](tb-getbuttontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
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

 

