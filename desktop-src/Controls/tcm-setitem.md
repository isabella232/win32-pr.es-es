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
ms.openlocfilehash: c27f93e2743e5676c0fcca932cfa1936bb72667ef4fa4a5334eaae3e78d2be08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876334"
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

Puntero a una [**estructura TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que contiene los nuevos atributos de elemento. El **miembro mask** especifica qué atributos se establecerán. Si el **miembro mask** especifica el valor TEXT de TCIF, el miembro pszText es la dirección de una cadena terminada en NULL y el miembro \_ **cchTextMax** se omite. 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TCM \_ SETITEMW** (Unicode) y **TCM \_ SETITEMA** (ANSI)<br/>                   |



 

 





