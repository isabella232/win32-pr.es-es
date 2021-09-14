---
title: TCM_SETITEM mensaje (Commctrl.h)
description: Establece algunos o todos los atributos de una pestaña. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetItem.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166209"
---
# <a name="tcm_setitem-message"></a>Mensaje \_ SETITEM de TCM

Establece algunos o todos los atributos de una pestaña. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que contiene los nuevos atributos de elemento. El **miembro mask** especifica qué atributos se establecerán. Si el **miembro mask** especifica el valor TCIF TEXT, el miembro pszText es la dirección de una cadena terminada en NULL y se omite el miembro \_ **cchTextMax.** 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TCM \_ SETITEMW** (Unicode) y **TCM \_ SETITEMA** (ANSI)<br/>                   |



 

 





