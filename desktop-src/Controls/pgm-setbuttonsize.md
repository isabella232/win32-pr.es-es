---
title: PGM_SETBUTTONSIZE mensaje (Commctrl.h)
description: Establece el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro Pager \_ SetButtonSize.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b120ed4bd6b7090621e09dd24b9e6a23b037fb5aed83e7ac6fc43254393330e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046795"
---
# <a name="pgm_setbuttonsize-message"></a>Mensaje \_ SETBUTTONSIZE de PGM

Establece el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ SetButtonSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de tipo **int** que contiene el nuevo tamaño de botón, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor int** que contiene el tamaño del botón anterior, en píxeles.

## <a name="remarks"></a>Comentarios

Si el control de paginación tiene el estilo [**\_ HORZ de PGS,**](pager-control-styles.md) el tamaño del botón determina el ancho de los botones de paginación. Si el control de paginación tiene el estilo [**\_ VERT de PGS,**](pager-control-styles.md) el tamaño del botón determina el alto de los botones de paginación. De forma predeterminada, el control de paginación establece su tamaño de botón en tres cuartos del ancho de la barra de desplazamiento.

Hay un tamaño mínimo para el botón de paginación, actualmente 12 píxeles. Sin embargo, esto puede cambiar, por lo que no debe depender de este valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





