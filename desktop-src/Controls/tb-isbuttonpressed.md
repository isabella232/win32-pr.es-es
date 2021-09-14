---
title: TB_ISBUTTONPRESSED mensaje (Commctrl.h)
description: Determina si se presiona el botón especificado en una barra de herramientas.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- TB_ISBUTTONPRESSED controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc2e6ec7b56ce205f3d89bc22a7c9dbbee90b1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166694"
---
# <a name="tb_isbuttonpressed-message"></a>Mensaje \_ ISBUTTONPRESSED de TB

Determina si se presiona el botón especificado en una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se presiona el botón o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





