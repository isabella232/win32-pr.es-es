---
title: EM_SETBKGNDCOLOR mensaje (Richedit.h)
description: El mensaje EM \_ SETBNDCOLOR establece el color de fondo para un control de edición enriquecido.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173c2da9f3c04e49211224bd269d79c0634e1cb3f8ea959f6b58e354fdf0dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412659"
---
# <a name="em_setbkgndcolor-message"></a>Mensaje \_ EM SETBANDERNDCOLOR

El **mensaje EM \_ SETBNDCOLOR** establece el color de fondo para un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se debe usar el color del sistema. Si este parámetro es un valor distinto de cero, el fondo se establece en el color del sistema de fondo de la ventana. De lo contrario, el fondo se establece en el color especificado.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**COLORREF**](/windows/desktop/gdi/colorref) que especifica el color si *wParam* es cero. Para generar un **COLORREF**, use la [**macro RGB.**](/windows/desktop/api/wingdi/nf-wingdi-rgb)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el color de fondo original.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

