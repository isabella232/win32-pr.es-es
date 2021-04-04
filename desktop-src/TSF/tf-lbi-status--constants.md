---
title: Constantes de TF_LBI_STATUS_ (Ctfutb. h)
description: Las constantes de TF \_ LBI \_ status \_ indican el estado de un elemento de la barra de idioma. Estos valores se usan con el método GetStatus de ITfLangBarItem.
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
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803343"
---
# <a name="tf_lbi_status_-constants"></a>TF \_ LBI \_ ( \_ constantes de estado) \*

Las constantes ** \_ TF \_ LBI \_ \* status* _ indican el estado de un elemento de la barra de idioma. Estos valores se usan con el método [ITfLangBarItem:: getStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .



| Constante o valor                                                                                                                                                                                                                                                       | Descripción                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <dt>_ * TF \_ Estado de LBI \_ \_ oculto * *</dt> <dt>0x00000001</dt> </dl>                 | El elemento está oculto. Este estilo se omite si el elemento no incluye el \_ estilo HIDDENSTATUSCONTROL de TF LBI \_ \_ .<br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <dt>**TF \_ Estado de LBI \_ \_ deshabilitado**</dt> <dt>0x00000002</dt> </dl>           | El elemento está deshabilitado.<br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <dt>**TF \_ Estado de LBI \_ \_ BTN \_**</dt> <dt>0x00010000</dt> </dl> | El elemento está en el estado de alternado u presionado. Este estilo se omite si el elemento no incluye el estilo de alternancia de tipo de comando TF \_ LBI \_ \_ \_ .<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





