---
title: Mensaje de EM_SETMARGINS (Winuser. h)
description: Establece el ancho de los márgenes izquierdo y derecho de un control de edición. El mensaje vuelve a dibujar el control para reflejar los nuevos márgenes. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS controles de mensajes de Windows
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
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996565"
---
# <a name="em_setmargins-message"></a>\_Mensaje SETMARGINS em

Establece el ancho de los márgenes izquierdo y derecho de un control de edición. El mensaje vuelve a dibujar el control para reflejar los nuevos márgenes. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Márgenes que se van a establecer. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**LEFTMARGIN de EC \_**</dt> </dl>    | Establece el margen izquierdo.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**RIGHTMARGIN de EC \_**</dt> </dl> | Establece el margen derecho.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**USEFONTINFO de EC \_**</dt> </dl> | **Controles Rich Edit:** Establece los márgenes izquierdo y derecho en un ancho estrecho calculado con las métricas de texto de la fuente actual del control. Si no se ha establecido ninguna fuente para el control, los márgenes se establecen en cero. Se omite el parámetro *lParam* . <br/> **Controles de edición:** El **valor \_ USEFONTINFO de EC** no se puede usar en el parámetro *wParam* . Solo se puede usar en el parámetro *lParam* .<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el nuevo ancho del margen izquierdo, en píxeles. Este valor se omite si *wParam* no incluye los valores de **\_ LEFTMARGIN de EC**.

**Edite los controles y la edición enriquecida 3,0 y versiones posteriores:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) puede especificar el valor **\_ USEFONTINFO de EC** para establecer el margen izquierdo en un ancho estrecho calculado con las métricas de texto de la fuente actual del control. Si no se ha establecido ninguna fuente para el control, el margen se establece en cero.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el nuevo ancho del margen derecho, en píxeles. Este valor se omite si *wParam* no incluye el **\_ RIGHTMARGIN de EC**.

**Edite los controles y la edición enriquecida 3,0 y versiones posteriores:** [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) puede especificar el valor **\_ USEFONTINFO de EC** para establecer el margen derecho en un ancho estrecho calculado con las métricas de texto de la fuente actual del control. Si no se ha establecido ninguna fuente para el control, el margen se establece en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

**Controles de edición:** No se puede **usar \_ USEFONTINFO de EC** en el parámetro *wParam* , pero se puede usar en el parámetro *lParam* .

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Todas las versiones de edición enriquecidas admiten el uso de **\_ USEFONTINFO de EC** en el parámetro *wParam* . Sin embargo, solo Microsoft Rich Edit 3,0 y versiones posteriores admiten el uso de **\_ USEFONTINFO de EC** en el parámetro *lParam* . Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETMARGINS em**](em-getmargins.md)
</dt> </dl>

 

