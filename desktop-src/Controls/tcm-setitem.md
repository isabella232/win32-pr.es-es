---
title: Mensaje de TCM_SETITEM (commctrl. h)
description: Establece algunos o todos los atributos de una pestaña. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ setItem.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801064"
---
# <a name="tcm_setitem-message"></a>\_Mensaje SETITEM de TCM

Establece algunos o todos los atributos de una pestaña. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que contiene los nuevos atributos de elemento. El miembro **Mask** especifica los atributos que se van a establecer. Si el miembro **Mask** especifica el \_ valor de texto TCIF, el miembro **miembros pszText** es la dirección de una cadena terminada en NULL y se omite el miembro **cchTextMax** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TCM \_ SETITEMW** (Unicode) y **TCM \_ SETITEMA** (ANSI)<br/>                   |



 

 





