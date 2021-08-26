---
title: EM_CHARFROMPOS mensaje (Winuser.h)
description: Obtiene información sobre el carácter más cercano a un punto especificado en el área de cliente de un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- EM_CHARFROMPOS controles de Windows mensaje
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
ms.openlocfilehash: 3a133907b29857abdc1663d3283bc4b4164878f3fa0976769e6d42daef2c4cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915965"
---
# <a name="em_charfrompos-message"></a>Mensaje \_ CHARFROMPOS EM

Obtiene información sobre el carácter más cercano a un punto especificado en el área de cliente de un control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Coordenadas de un punto en el área cliente del control. Las coordenadas están en unidades de pantalla y son relativas a la esquina superior izquierda del área cliente del control.

**Controles de edición enriquecciones:** Puntero a una [**estructura POINTL**](/previous-versions//dd162807(v=vs.85)) que contiene las coordenadas horizontal y vertical.

**Editar controles:** Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la coordenada horizontal. HIWORD [**contiene la**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) coordenada vertical.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**Controles de edición enriquecciones:** El valor devuelto especifica el índice de caracteres de base cero del carácter más cercano al punto especificado. El valor devuelto indica el último carácter del control de edición si el punto especificado está más allá del último carácter del control.

**Editar controles:** Loword [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el índice de base cero del carácter más cercano al punto especificado. Este índice es relativo al principio del control, no al principio de la línea. Si el punto especificado está más allá del último carácter del control de edición, el valor devuelto indica el último carácter del control. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el índice de base cero de la línea que contiene el carácter. Para los controles de edición de una sola línea, este valor es cero. El índice indica el delimitador de línea si el punto especificado está más allá del último carácter visible de una línea.

## <a name="remarks"></a>Comentarios

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

Si se pasa un punto a **EM \_ CHARFROMPOS** como *lParam* y el punto está fuera de los límites del control de edición, *lResult* es (65535, 65535).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ POSFROMCHAR**](em-posfromchar.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

