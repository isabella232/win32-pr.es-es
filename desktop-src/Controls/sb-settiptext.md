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
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167101"
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

## <a name="remarks"></a>Observaciones

Este texto de información sobre herramientas se muestra en dos situaciones:

-   Cuando el panel correspondiente de la barra de estado solo contiene un icono.
-   Cuando el panel correspondiente de la barra de estado contiene texto truncado debido al tamaño del panel.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ SETTIPTEXTW** (Unicode) y **SB \_ SETTIPTEXTA** (ANSI)<br/>               |



 

 





