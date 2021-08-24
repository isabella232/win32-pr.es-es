---
title: Constantes de radiofrecuencia (CommCtrl.h)
description: Estas constantes se usan como valores devueltos por un control en respuesta a un código de \_ notificación NM CUSTOMDRAW.
ms.assetid: 6b05e27e-5d18-46f2-b326-2a5148597852
topic_type:
- apiref
api_name:
- CDRF_DODEFAULT
- CDRF_NEWFONT
- CDRF_SKIPDEFAULT
- CDRF_DOERASE
- CDRF_NOTIFYPOSTPAINT
- CDRF_NOTIFYITEMDRAW
- CDRF_NOTIFYSUBITEMDRAW
- CDRF_NOTIFYPOSTERASE
- CDRF_SKIPPOSTPAINT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817bab7c2ec41134d71c92ada94c62475b01cc2db96a9f8c74ecb2c7b9274451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770385"
---
# <a name="rf-constants"></a>Constantes de radiofrecuencia

Estas constantes se usan como valores devueltos por un control en respuesta a un código [de \_ notificación NM CUSTOMDRAW.](nm-customdraw.md)



| Constante o valor                                                                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CDRF_DODEFAULT"></span><span id="cdrf_dodefault"></span><dl> <dt>**CDRF \_ DoDEFAULT**</dt> <dt>0x00000000</dt> </dl>                         | El control se dibujará a sí mismo. No enviará ningún código de notificación [DE NM \_ CUSTOMDRAW](nm-customdraw.md) adicional para este ciclo de pintura. Esto sucede cuando **dwDrawStage de** la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                               |
| <span id="CDRF_NEWFONT"></span><span id="cdrf_newfont"></span><dl> <dt>**CDRF \_ NewFONT**</dt> <dt>0x00000002</dt> </dl>                               | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, vea Cambio de fuentes y colores. Esto sucede cuando **dwDrawStage de** la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) es igual a \_ CDDS ITEMPREPAINT.<br/>                                                                                                                                      |
| <span id="CDRF_SKIPDEFAULT"></span><span id="cdrf_skipdefault"></span><dl> <dt>**CDRF \_ SkipDEFAULT**</dt> <dt>0x00000004</dt> </dl>                   | La aplicación ha dibujado el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage de** la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) es igual a \_ CDDS ITEMPREPAINT.<br/>                                                                                                                                                                                                                          |
| <span id="CDRF_DOERASE"></span><span id="cdrf_doerase"></span><dl> <dt>**CDRF \_ DoERASE**</dt> <dt>0x00000008</dt> </dl>                               | **Windows Vista y versiones posteriores.** El control dibujará el fondo.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CDRF_NOTIFYPOSTPAINT"></span><span id="cdrf_notifypostpaint"></span><dl> <dt>**CDRF \_ NotifyPOSTPAINT**</dt> <dt>0x00000010</dt> </dl>       | El control notificará al elemento primario después de pintar un elemento. Esto sucede cuando **dwDrawStage de** la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                               |
| <span id="CDRF_NOTIFYITEMDRAW"></span><span id="cdrf_notifyitemdraw"></span><dl> <dt>**CDRF \_ NotifyITEMDRAW**</dt> <dt>0x00000020</dt> </dl>          | El control notificará al elemento primario las operaciones de dibujo relacionadas con elementos. Enviará códigos de [notificación NM \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar elementos. Esto sucede cuando **dwDrawStage de** la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) es igual a CDDS \_ PREPAINT.<br/>                                                                                                                           |
| <span id="CDRF_NOTIFYSUBITEMDRAW"></span><span id="cdrf_notifysubitemdraw"></span><dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> <dt>0x00000020</dt> </dl> | **Internet Explorer 4.0 y versiones posteriores.** El control notificará al elemento primario las operaciones de dibujo relacionadas con elementos. Enviará códigos de [notificación NM \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar elementos. Esto sucede cuando **dwDrawStage de** la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) es igual a CDDS \_ PREPAINT. Esta marca es idéntica a **CDRF \_ NOTIFYITEMDRAW** y su uso depende del contexto.<br/> |
| <span id="CDRF_NOTIFYPOSTERASE"></span><span id="cdrf_notifyposterase"></span><dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> <dt>0x00000040</dt> </dl>       | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage de** la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) es igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                                |
| <span id="CDRF_SKIPPOSTPAINT"></span><span id="cdrf_skippostpaint"></span><dl> <dt>**CDRF \_ SkipPOSTPAINT**</dt> <dt>0x00000100</dt> </dl>             | **Windows Vista y versiones posteriores.** El control no dibujará el rectángulo de foco.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Comentarios

Estas constantes se definen en Commctrl.h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Personalizar la apariencia de un control mediante un dibujo personalizado](custom-draw.md)
</dt> </dl>

 

 





