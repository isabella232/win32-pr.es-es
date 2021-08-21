---
title: TF_LBI_STATUS_ constantes (Ctfutb.h)
description: Las constantes TF \_ LBI \_ STATUS \ indican el estado de un elemento de la barra de \_ idioma. Estos valores se usan con el método ITfLangBarItem GetStatus.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c433a4c92333ed63251aebf0d633453c070a2410113bda923f5f6879b02fa83d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118874532"
---
# <a name="tf_lbi_status_-constants"></a>Constantes \_ de TF LBI \_ STATUS \_ \*

Las **constantes TF \_ LBI \_ STATUS \_ \*** indican el estado de un elemento de la barra de idioma. Estos valores se usan con el [método ITfLangBarItem::GetStatus.](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)



| Constante o valor                                                                                                                                                                                                                                                       | Descripción                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <dt>**TF \_ Estado de LBI \_ \_ oculto**</dt> <dt>0x00000001</dt> </dl>                 | El elemento está oculto. Este estilo se omite si el elemento no incluye el estilo TF \_ LBI \_ STYLE \_ HIDDENSTATUSCONTROL.<br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <dt>**TF \_ Estado de LBI \_ \_ deshabilitado**</dt> <dt>0x00000002</dt> </dl>           | El elemento está deshabilitado.<br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <dt>**TF \_ LBI \_ STATUS \_ BTN \_ TOGGLED**</dt> <dt>0x00010000</dt> </dl> | El elemento está en estado alternado o presionado. Este estilo se omite si el elemento no incluye el estilo TF \_ LBI \_ STYLE \_ BTN \_ TOGGLE.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>Ctfutb.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





