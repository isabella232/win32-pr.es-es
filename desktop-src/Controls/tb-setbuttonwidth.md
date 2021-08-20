---
title: TB_SETBUTTONWIDTH mensaje (Commctrl.h)
description: Establece los anchos de botón mínimo y máximo en el control de barra de herramientas.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH controles de Windows mensaje
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
ms.openlocfilehash: 145ae1459b76fba60dd76b34e36d222cf62b93af071f2b430321d86956a3a871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167600"
---
# <a name="tb_setbuttonwidth-message"></a>Mensaje \_ SETBUTTONWIDTH de TB

Establece los anchos de botón mínimo y máximo en el control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica el**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ancho mínimo del botón, en píxeles. Los botones de la barra de herramientas nunca serán más estrechos que este valor.

HIWORD [**especifica el**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ancho máximo del botón, en píxeles. Si el texto del botón es demasiado ancho, el control lo muestra con puntos suspensivos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

Use **TB \_ SETBUTTONWIDTH para** establecer los anchos máximos y mínimos permitidos para los botones antes de agregarse. Use [**TB \_ SETBUTTONSIZE para**](tb-setbuttonsize.md) establecer el tamaño real de los botones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

