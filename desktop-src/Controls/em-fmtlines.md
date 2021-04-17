---
title: Mensaje de EM_FMTLINES (Winuser. h)
description: Establece una marca que determina si un control de edición multilínea incluye caracteres de salto de línea automáticos. Un salto de línea flexible se compone de dos retornos de carro y un avance de línea, y se inserta al final de una línea que se rompe debido a aparecen.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- EM_FMTLINES controles de mensajes de Windows
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
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491009"
---
# <a name="em_fmtlines-message"></a>\_Mensaje FMTLINES em

Establece una marca que determina si un control de edición multilínea incluye caracteres de salto de línea automáticos. Un salto de línea flexible se compone de dos retornos de carro y un avance de línea, y se inserta al final de una línea que se rompe debido a aparecen.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si se van a insertar caracteres de salto de línea. Un valor **true** inserta los caracteres; Si el valor **es false** , se quitan.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es idéntico al parámetro *wParam* .

## <a name="remarks"></a>Observaciones

Este mensaje solo afecta al búfer devuelto por el mensaje de [**\_ GETHANDLE em**](em-gethandle.md) y el texto devuelto por el mensaje de [**\_ GETTEXT de WM**](/windows/desktop/winmsg/wm-gettext) . No tiene ningún efecto en la presentación del texto en el control de edición.

El **mensaje \_ FMTLINES em** no afecta a una línea que termina con un salto de línea fuerte. Un salto de línea fuerte se compone de un retorno de carro y un avance de línea.

> [!Note]  
> El tamaño del texto cambia cuando se procesa este mensaje.

 

**Edición enriquecida:** No se admite el mensaje **\_ FMTLINES em** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GETHANDLE (EM) \_**](em-gethandle.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**GETTEXT de WM \_**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

