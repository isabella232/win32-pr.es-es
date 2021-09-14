---
title: TB_CUSTOMIZE mensaje (Commctrl.h)
description: Muestra el cuadro de diálogo Personalizar barra de herramientas .
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- TB_CUSTOMIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166877"
---
# <a name="tb_customize-message"></a>Mensaje CUSTOMIZE de TB \_

Muestra el cuadro **de diálogo Personalizar barra** de herramientas .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!Note]  
> La barra de herramientas debe controlar [las notificaciones \_ QUERYINSERT](tbn-queryinsert.md) y [TBN \_ QUERYDELETE](tbn-querydelete.md) de TBN para que aparezca el cuadro de diálogo Personalizar barra de herramientas.  Si la barra de herramientas no controla esas notificaciones, **TB \_ CUSTOMIZE** no tiene ningún efecto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





