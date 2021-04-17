---
title: Mensaje de TCM_SETMINTABWIDTH (commctrl. h)
description: Establece el ancho mínimo de los elementos de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetMinTabWidth.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- TCM_SETMINTABWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656460"
---
# <a name="tcm_setmintabwidth-message"></a>\_Mensaje SETMINTABWIDTH de TCM

Establece el ancho mínimo de los elementos de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Ancho mínimo que se va a establecer para un elemento de control de pestaña. Si este parámetro se establece en-1, el control usará el ancho de tabulación predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa el ancho mínimo de tabulación anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





