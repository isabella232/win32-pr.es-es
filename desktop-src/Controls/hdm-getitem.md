---
title: Mensaje de HDM_GETITEM (commctrl. h)
description: Obtiene información sobre un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetItem de encabezado.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- HDM_GETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150318"
---
# <a name="hdm_getitem-message"></a>HDM \_ mensaje GETITEM

Obtiene información sobre un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetItem de encabezado**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento para el que se va a recuperar información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Cuando se envía el mensaje, el miembro de la **máscara** indica el tipo de información que se solicita. Cuando el mensaje vuelve, los demás miembros reciben la información solicitada. Si el miembro de la **máscara** especifica cero, el mensaje devuelve **true** pero no copia ninguna información en la estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si la \_ marca de texto HDI se establece en el miembro **Mask** de la estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , el control puede cambiar el miembro **miembros pszText** de la estructura para que apunte al nuevo texto en lugar de llenar el búfer con el texto solicitado. Las aplicaciones no deben suponer que el texto siempre se colocará en el búfer solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDM \_ GETITEMW** (Unicode) y **HDM \_ GETITEMA** (ANSI)<br/>                   |



 

 





