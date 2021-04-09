---
title: Mensaje de SB_GETTIPTEXT (commctrl. h)
description: Recupera el texto de información sobre herramientas de un elemento de una barra de estado. La barra de estado se debe crear con el \_ estilo de información sobre herramientas de SBT para habilitar la información sobre herramientas.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT controles de mensajes de Windows
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
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905458"
---
# <a name="sb_gettiptext-message"></a>\_Mensaje GETTIPTEXT de SB

Recupera el texto de información sobre herramientas de un elemento de una barra de estado. La barra de estado se debe crear con el estilo de [**\_ información sobre herramientas de SBT**](status-bar-styles.md) para habilitar la información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el índice de base cero del elemento que recibe el texto de información sobre herramientas. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el tamaño del búfer en *lParam*, en caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer de caracteres que recibe el texto de información sobre herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso incorrecto de este mensaje puede producir problemas en la aplicación. Por ejemplo, si el texto es demasiado grande para el búfer *lParam* , podría producirse un desbordamiento del búfer. Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ GETTIPTEXTW** (Unicode) y **SB \_ GETTIPTEXTA** (ANSI)<br/>               |



 

