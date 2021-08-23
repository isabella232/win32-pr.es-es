---
title: SB_GETTIPTEXT mensaje (Commctrl.h)
description: Recupera el texto de información sobre herramientas de un elemento de una barra de estado. La barra de estado debe crearse con el estilo SBT \_ TOOLTIPS para habilitar la información sobre herramientas.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a78fa6650d850cad2b6de8cc77f1d44b49b8325bf6856b989953fc6511f56f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637135"
---
# <a name="sb_gettiptext-message"></a>Mensaje \_ SB GETTIPTEXT

Recupera el texto de información sobre herramientas de un elemento de una barra de estado. La barra de estado debe crearse con el estilo [**SBT \_ TOOLTIPS**](status-bar-styles.md) para habilitar la información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el índice de base cero del elemento que recibe el texto de información sobre herramientas. HIWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el tamaño del búfer en *lParam*, en caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer de caracteres que recibe el texto de información sobre herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Comentarios

**Advertencia de seguridad:** El uso incorrecto de este mensaje puede causar problemas en la aplicación. Por ejemplo, si el texto es demasiado grande para el búfer *lParam,* podría provocar un desbordamiento del búfer. Debe revisar consideraciones [de seguridad: Microsoft Windows antes](sec-comctls.md) de continuar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ GETTIPTEXTW** (Unicode) y **SB \_ GETTIPTEXTA** (ANSI)<br/>               |



 

