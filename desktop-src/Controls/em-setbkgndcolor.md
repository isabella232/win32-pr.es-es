---
title: EM_SETBKGNDCOLOR mensaje (Richedit.h)
description: El mensaje EM \_ SETBCONTROLNDCOLOR establece el color de fondo de un control de edición enriquecido.
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
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062131"
---
# <a name="em_setbkgndcolor-message"></a>Mensaje \_ EM SETBNDCOLOR

El **mensaje EM \_ SETBCONTROLNDCOLOR** establece el color de fondo de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se debe usar el color del sistema. Si este parámetro es un valor distinto de cero, el fondo se establece en el color del sistema de fondo de la ventana. De lo contrario, el fondo se establece en el color especificado.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**COLORREF**](/windows/desktop/gdi/colorref) que especifica el color si *wParam* es cero. Para generar un **COLORREF,** use la [**macro RGB.**](/windows/desktop/api/wingdi/nf-wingdi-rgb)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve el color de fondo original.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

