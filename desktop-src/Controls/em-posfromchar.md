---
title: Mensaje de EM_POSFROMCHAR (Winuser. h)
description: Recupera las coordenadas del área de cliente de un carácter especificado en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534366"
---
# <a name="em_posfromchar-message"></a>\_Mensaje POSFROMCHAR em

Recupera las coordenadas del área de cliente de un carácter especificado en un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Edición enriquecida 1,0 y 3,0:** Puntero a una estructura [**Pointl**](/previous-versions//dd162807(v=vs.85)) que recibe las coordenadas del área de cliente del carácter. Las coordenadas están en unidades de pantalla y son relativas a la esquina superior izquierda del área cliente del control.

**Controles de edición y edición enriquecida 2,0:** Índice de base cero del carácter.

</dd> <dt>

*lParam* 
</dt> <dd>

**Edición enriquecida 1,0 y 3,0:** Índice de base cero del carácter.

**Controles de edición y edición enriquecida 2,0:** Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**Edición enriquecida 1,0 y 3,0:** No se utiliza el valor devuelto.

**Controles de edición y edición enriquecida 2,0:** El valor devuelto contiene las coordenadas del área del cliente del carácter. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordenada horizontal y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordenada vertical.

## <a name="remarks"></a>Observaciones

Una coordenada devuelta puede ser un valor negativo si el carácter especificado no se muestra en el área cliente del control de edición. Las coordenadas se truncan en valores enteros.

Si el carácter es un delimitador de línea, las coordenadas devueltas indican un punto situado más allá del último carácter visible de la línea. Si el índice especificado es mayor que el índice del último carácter del control, el control devuelve-1.

**Edición enriquecida 3,0 y versiones posteriores:** Por compatibilidad con versiones anteriores, Microsoft Rich Edit 3,0 admite la sintaxis que usa Microsoft Rich Edit 2,0. Si Microsoft Rich Edit 3,0 detecta que *wParam* no es un puntero [**Pointl**](/previous-versions//dd162807(v=vs.85)) válido, se supone que el mensaje se envió con la sintaxis de Microsoft Rich Edit 2,0. En este caso, utiliza el valor devuelto para devolver las coordenadas.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

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

[**\_CHARFROMPOS em**](em-charfrompos.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**PUNTO**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

