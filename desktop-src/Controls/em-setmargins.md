---
title: EM_SETMARGINS mensaje (Winuser.h)
description: Establece los anchos de los márgenes izquierdo y derecho de un control de edición. El mensaje vuelve a dibujar el control para reflejar los nuevos márgenes. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396bba6dda0f6dbd132b9f67fa5a1ef012758bbf7cf8fa9517b656dcf164c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048365"
---
# <a name="em_setmargins-message"></a>Mensaje \_ SETMARGINS DE EM

Establece los anchos de los márgenes izquierdo y derecho de un control de edición. El mensaje vuelve a dibujar el control para reflejar los nuevos márgenes. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Márgenes que se establecerán. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**EC \_ LEFTMARGIN**</dt> </dl>    | Establece el margen izquierdo.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**EC \_ RIGHTMARGIN**</dt> </dl> | Establece el margen derecho.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**EC \_ USEFONTINFO**</dt> </dl> | **Controles de edición enriquecciones:** Establece los márgenes izquierdo y derecho en un ancho estrecho calculado mediante las métricas de texto de la fuente actual del control. Si no se ha establecido ninguna fuente para el control, los márgenes se establecen en cero. Se *omite el parámetro lParam.* <br/> **Editar controles:** El **valor \_ USEFONTINFO de EC** no se puede usar en el parámetro *wParam.* Solo se puede usar en el *parámetro lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el nuevo ancho del margen izquierdo, en píxeles. Este valor se omite si *wParam* no incluye **EC \_ LEFTMARGIN.**

**Editar controles y Rich Edit 3.0 y versiones posteriores:** LOWORD [**puede especificar**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el valor **\_ USEFONTINFO de EC** para establecer el margen izquierdo en un ancho estrecho calculado mediante las métricas de texto de la fuente actual del control. Si no se ha establecido ninguna fuente para el control, el margen se establece en cero.

HIWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el nuevo ancho del margen derecho, en píxeles. Este valor se omite si *wParam* no incluye **EC \_ RIGHTMARGIN.**

**Editar controles y Rich Edit 3.0 y versiones posteriores:** [**HIWORD puede especificar**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el valor **\_ USEFONTINFO de EC** para establecer el margen derecho en un ancho estrecho calculado mediante las métricas de texto de la fuente actual del control. Si no se ha establecido ninguna fuente para el control, el margen se establece en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

**Editar controles:** No puede usar **EC \_ USEFONTINFO en** el parámetro *wParam,* pero puede usarlo en el *parámetro lParam.*

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Todas las versiones de edición enriquecciones admiten **el uso de EC \_ USEFONTINFO en** el parámetro *wParam.* Sin embargo, solo Microsoft Rich Edit 3.0 y versiones posteriores admiten el uso de **\_ EC USEFONTINFO** en el *parámetro lParam.* Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETMARGINS**](em-getmargins.md)
</dt> </dl>

 

