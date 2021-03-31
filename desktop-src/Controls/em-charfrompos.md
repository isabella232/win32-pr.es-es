---
title: Mensaje de EM_CHARFROMPOS (Winuser. h)
description: Obtiene información sobre el carácter más cercano a un punto especificado en el área cliente de un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- EM_CHARFROMPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491500"
---
# <a name="em_charfrompos-message"></a>\_Mensaje CHARFROMPOS em

Obtiene información sobre el carácter más cercano a un punto especificado en el área cliente de un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Coordenadas de un punto en el área cliente del control. Las coordenadas están en unidades de pantalla y son relativas a la esquina superior izquierda del área cliente del control.

**Controles Rich Edit:** Puntero a una estructura [**Pointl**](/previous-versions//dd162807(v=vs.85)) que contiene las coordenadas horizontal y vertical.

**Controles de edición:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordenada horizontal. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordenada vertical.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**Controles Rich Edit:** El valor devuelto especifica el índice de carácter de base cero del carácter más próximo al punto especificado. El valor devuelto indica el último carácter del control de edición si el punto especificado está más allá del último carácter del control.

**Controles de edición:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el índice de base cero del carácter más próximo al punto especificado. Este índice es relativo al principio del control, no al principio de la línea. Si el punto especificado está más allá del último carácter del control de edición, el valor devuelto indica el último carácter del control. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el índice de base cero de la línea que contiene el carácter. En el caso de los controles de edición de una sola línea, este valor es cero. El índice indica el delimitador de línea si el punto especificado está más allá del último carácter visible de una línea.

## <a name="remarks"></a>Observaciones

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

Si se pasa un punto a **em \_ CHARFROMPOS** como *lParam* y el punto está fuera de los límites del control de edición, el *lResult* es (65535, 65535).

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

[**\_POSFROMCHAR em**](em-posfromchar.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**PUNTO**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

