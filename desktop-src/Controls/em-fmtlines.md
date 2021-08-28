---
title: EM_FMTLINES mensaje (Winuser.h)
description: Establece una marca que determina si un control de edición multilínea incluye caracteres de salto de línea flexibles. Un salto de línea suave consta de dos retornos de carro y un avance de línea, y se inserta al final de una línea que se divide debido al encapsulado de palabras.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- EM_FMTLINES controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e0c0c410f13a33f0e387098178b42faaf3269c36d11f75e765eb753fa9d0844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545105"
---
# <a name="em_fmtlines-message"></a>Mensaje \_ DE EM FMTLINES

Establece una marca que determina si un control de edición multilínea incluye caracteres de salto de línea flexibles. Un salto de línea suave consta de dos retornos de carro y un avance de línea, y se inserta al final de una línea que se divide debido al encapsulado de palabras.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se van a insertar caracteres de salto de línea flexibles. Un valor **true inserta** los caracteres; Un valor **de FALSE** los quita.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es idéntico al *parámetro wParam.*

## <a name="remarks"></a>Comentarios

Este mensaje solo afecta al búfer devuelto por el [**mensaje EM \_ GETHANDLE**](em-gethandle.md) y al texto devuelto por el [**mensaje \_ GETTEXT de WM.**](/windows/desktop/winmsg/wm-gettext) No tiene ningún efecto en la presentación del texto dentro del control de edición.

El **mensaje EM \_ FMTLINES** no afecta a una línea que termina con un salto de línea duro. Un salto de línea duro consta de un retorno de carro y un avance de línea.

> [!Note]  
> El tamaño del texto cambia cuando se procesa este mensaje.

 

**Edición enriquecte:** No se admite el mensaje **\_ EM FMTLINES.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETHANDLE**](em-gethandle.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

