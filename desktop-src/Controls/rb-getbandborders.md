---
title: Mensaje de RB_GETBANDBORDERS (commctrl. h)
description: Recupera los bordes de una banda. El resultado de este mensaje se puede usar para calcular el área utilizable en una banda.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996724"
---
# <a name="rb_getbandborders-message"></a>Mensaje de GETBANDBORDERS de RB \_

Recupera los bordes de una banda. El resultado de este mensaje se puede usar para calcular el área utilizable en una banda.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda para la que se van a recuperar los bordes.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá los bordes de banda. Si el control rebar tiene el [**estilo \_ BANDBORDERS de RBS**](rebar-control-styles.md) , cada miembro de esta estructura recibirá el número de píxeles, en el lado correspondiente de la banda, que conforman el borde. Si el control rebar no tiene el estilo **\_ BANDBORDERS de RBS** , solo el miembro **izquierdo** de esta estructura recibe información válida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

