---
title: Mensaje de TB_CUSTOMIZE (commctrl. h)
description: Muestra el cuadro de diálogo Personalizar barra de herramientas.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- TB_CUSTOMIZE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658404"
---
# <a name="tb_customize-message"></a>TB \_ personalizar mensaje

Muestra el cuadro de diálogo **personalizar barra de herramientas** .

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
> La barra de herramientas debe controlar las notificaciones [TBN \_ QUERYINSERT](tbn-queryinsert.md) y [TBN \_ QUERYDELETE](tbn-querydelete.md) para que aparezca el cuadro de diálogo **personalizar barra de herramientas** . Si la barra de herramientas no controla esas notificaciones, la **\_ Personalización de TB** no tiene ningún efecto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





