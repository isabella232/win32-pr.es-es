---
title: Mensaje de TB_SETBUTTONWIDTH (commctrl. h)
description: Establece los anchos de botón mínimo y máximo en el control de barra de herramientas.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150312"
---
# <a name="tb_setbuttonwidth-message"></a>\_Mensaje SETBUTTONWIDTH TB

Establece los anchos de botón mínimo y máximo en el control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el ancho mínimo del botón, en píxeles. Los botones de la barra de herramientas nunca serán más estrechos que este valor.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el ancho máximo del botón, en píxeles. Si el texto del botón es demasiado ancho, el control lo muestra con puntos suspensivos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

Use **TB \_ SETBUTTONWIDTH** para establecer los anchos máximo y mínimo permitidos para los botones antes de agregarlos. Use [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) para establecer el tamaño real de los botones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

