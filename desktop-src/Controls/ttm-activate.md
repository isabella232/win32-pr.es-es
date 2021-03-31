---
title: Mensaje de TTM_ACTIVATE (commctrl. h)
description: Activa o desactiva un control de información sobre herramientas.
ms.assetid: f37da001-748c-4c51-bb32-dc49031ff2fb
keywords:
- TTM_ACTIVATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_ACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e200b769cd3d9e07cb63a5a540960bcc707f862d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079392"
---
# <a name="ttm_activate-message"></a>TTM \_ Activar mensaje

Activa o desactiva un control de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca de activación. Si este parámetro es **true**, se activa el control ToolTip. Si es **false**, se desactiva el control ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





