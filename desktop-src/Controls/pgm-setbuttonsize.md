---
title: Mensaje de PGM_SETBUTTONSIZE (commctrl. h)
description: Establece el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro SetButtonSize de buscapersonas \_ .
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE controles de mensajes de Windows
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
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534030"
---
# <a name="pgm_setbuttonsize-message"></a>\_Mensaje SETBUTTONSIZE PGM

Establece el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetButtonSize de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de tipo **int** que contiene el nuevo tamaño de botón, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **int** que contiene el tamaño de botón anterior, en píxeles.

## <a name="remarks"></a>Observaciones

Si el control de paginación tiene el estilo [**págs \_ horizontal**](pager-control-styles.md) , el tamaño del botón determina el ancho de los botones de paginación. Si el control de paginación tiene el estilo [**págs \_ Vert**](pager-control-styles.md) , el tamaño del botón determina el alto de los botones de paginación. De forma predeterminada, el control de paginación establece su tamaño de botón en tres cuartos del ancho de la barra de desplazamiento.

Hay un tamaño mínimo para el botón de buscapersonas; actualmente, 12 píxeles. Sin embargo, esto puede cambiar, por lo que no debe depender de este valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETBUTTONSIZE PGM**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





