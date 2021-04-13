---
title: Mensaje de SB_SETTIPTEXT (commctrl. h)
description: Establece el texto de información sobre herramientas para un elemento de una barra de estado. La barra de estado se debe haber creado con el \_ estilo de información sobre herramientas de SBT para habilitar la información sobre herramientas.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- SB_SETTIPTEXT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491987"
---
# <a name="sb_settiptext-message"></a>\_Mensaje SETTIPTEXT de SB

Establece el texto de información sobre herramientas para un elemento de una barra de estado. La barra de estado se debe haber creado con el estilo de [**\_ información sobre herramientas de SBT**](status-bar-styles.md) para habilitar la información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento que recibirá el texto de información sobre herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer de caracteres que contiene el nuevo texto de información sobre herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="remarks"></a>Observaciones

Este texto de información sobre herramientas se muestra en dos situaciones:

-   Cuando el panel correspondiente de la barra de estado solo contiene un icono.
-   Cuando el panel correspondiente de la barra de estado contiene texto truncado debido al tamaño del panel.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ SETTIPTEXTW** (Unicode) y **SB \_ SETTIPTEXTA** (ANSI)<br/>               |



 

 





