---
title: EM_POSFROMCHAR mensaje (Winuser.h)
description: Recupera las coordenadas de área de cliente de un carácter especificado en un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062152"
---
# <a name="em_posfromchar-message"></a>Mensaje \_ DE EM POSFROMCHAR

Recupera las coordenadas de área de cliente de un carácter especificado en un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 1.0 y 3.0:** Puntero a una [**estructura POINTL**](/previous-versions//dd162807(v=vs.85)) que recibe las coordenadas de área de cliente del carácter. Las coordenadas están en unidades de pantalla y son relativas a la esquina superior izquierda del área cliente del control.

**Editar controles y Rich Edit 2.0:** Índice de base cero del carácter.

</dd> <dt>

*lParam* 
</dt> <dd>

**Rich Edit 1.0 y 3.0:** Índice de base cero del carácter.

**Editar controles y Rich Edit 2.0:** Este parámetro no se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**Rich Edit 1.0 y 3.0:** No se usa el valor devuelto.

**Editar controles y Rich Edit 2.0:** El valor devuelto contiene las coordenadas del área de cliente del carácter. El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordenada horizontal y [**hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordenada vertical.

## <a name="remarks"></a>Observaciones

Una coordenada devuelta puede ser un valor negativo si el carácter especificado no se muestra en el área cliente del control de edición. Las coordenadas se truncan en valores enteros.

Si el carácter es un delimitador de línea, las coordenadas devueltas indican un punto justo después del último carácter visible en la línea. Si el índice especificado es mayor que el índice del último carácter del control, el control devuelve -1.

**Rich Edit 3.0 y versiones posteriores:** Por compatibilidad con versiones anteriores, Microsoft Rich Edit 3.0 admite la sintaxis que usa Microsoft Rich Edit 2.0. Si Microsoft Rich Edit 3.0 detecta que *wParam* no es un puntero [**POINTL**](/previous-versions//dd162807(v=vs.85)) válido, se supone que el mensaje se envió mediante la sintaxis de Microsoft Rich Edit 2.0. En este caso, usa el valor devuelto para devolver las coordenadas.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ CHARFROMPOS**](em-charfrompos.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

