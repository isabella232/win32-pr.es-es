---
title: SB_SETTIPTEXT mensaje (Commctrl.h)
description: Establece el texto de información sobre herramientas de un elemento en una barra de estado. La barra de estado debe haber sido creada con el estilo SBT \_ TOOLTIPS para habilitar la información sobre herramientas.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- SB_SETTIPTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 864ba53066b000f9f7ae65365341238a701b4e70bc4ce8cc70adba923d57a5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637025"
---
# <a name="sb_settiptext-message"></a>Mensaje \_ SB SETTIPTEXT

Establece el texto de información sobre herramientas de un elemento en una barra de estado. La barra de estado debe haber sido creada con el estilo [**SBT \_ TOOLTIPS**](status-bar-styles.md) para habilitar la información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que recibirá el texto de la información sobre herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer de caracteres que contiene el nuevo texto de información sobre herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Comentarios

Este texto de información sobre herramientas se muestra en dos situaciones:

-   Cuando el panel correspondiente de la barra de estado solo contiene un icono.
-   Cuando el panel correspondiente de la barra de estado contiene texto truncado debido al tamaño del panel.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ SETTIPTEXTW** (Unicode) y **SB \_ SETTIPTEXTA** (ANSI)<br/>               |



 

 





