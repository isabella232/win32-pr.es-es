---
title: Constantes de TF_LBI_ (Ctfutb. h)
description: Las constantes de TF \_ LBI \_ \ se usan con el método ITfLangBarItemSink de actualización para indicar qué elementos de la barra de idioma han cambiado.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685949"
---
# <a name="tf_lbi_-constants"></a>TF \_ LBI ( \_ \* constantes)

Las constantes ** \_ TF \_ \* LBI* _ se usan con el método [ITfLangBarItemSink:: ALUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) para indicar qué elementos de la barra de idioma han cambiado.



| Constante o valor                                                                                                                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <dt>_ * TF \_ Icono de LBI \_ * *</dt> <dt>0x00000001</dt> </dl>                                                        | El icono del elemento ha cambiado. La barra de idioma llama a [ITfLangBarItemButton:: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) en respuesta a esta notificación.<br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <dt>**TF \_ \_Texto LBI**</dt> <dt>0x00000002</dt> </dl>                                                        | El texto de un botón o elemento de botón de mapa de bits ha cambiado. La barra de idioma llama a [ITfLangBarItemButton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) o [ITfLangBarItemBitmapButton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), lo que sea adecuado, en respuesta a esta notificación.<br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <dt>**TF \_ \_Información sobre herramientas de LBI**</dt> <dt>0x00000004</dt> </dl>                                               | Texto de información sobre herramientas del elemento cambiado. La barra de idioma llama a [ITfLangBarItem:: GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) en respuesta a esta notificación.<br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <dt>**TF \_ \_Mapa de bits de LBI**</dt> <dt>0x00000008</dt> </dl>                                                  | El mapa de bits de un mapa de bits o un elemento de botón de mapa de bits cambiado. La barra de idioma llama a [ITfLangBarItemBitmap::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) o [ITfLangBarItemBitmapButton::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), según corresponda, en respuesta a esta notificación.<br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <dt>**TF \_ El \_ globo LBI**</dt> <dt>0x00000010</dt> </dl>                                               | La información de un elemento de globo ha cambiado. La barra de idioma llama a [ITfLangBarItemBalloon:: GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) en respuesta a esta notificación.<br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <dt>**TF \_ 0x00010000 de \_ Estado de LBI**</dt> <dt></dt> </dl>                                                  | El estado del elemento ha cambiado. La barra de idioma llama a [ITfLangBarItem:: getStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) en respuesta a esta notificación.<br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <dt>**TF \_ LBI \_ BMPALL**</dt> <dt>TF \_ LBI \_ mapa de bits \| TF \_ LBI \_ TOOLTIP</dt> </dl>                          | Combina la \_ \_ información sobre herramientas TF LBI Bitmap y TF \_ LBI \_ .<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <dt>**TF \_ LBI \_ BMPBTNALL**</dt> <dt>TF \_ LBI \_ Bitmap \| TF \_ LBI \_ texto \| TF \_ LBI \_ TOOLTIP</dt> </dl> | Combina los \_ \_ mapas de bits de TF LBI, TF \_ LBI \_ Text y TF \_ LBI \_ TOOLTIP.<br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <dt>**TF \_ LBI \_ BTNALL**</dt> <dt>TF \_ LBI \_ Icon \| TF \_ LBI \_ Text \| TF \_ LBI \_ TOOLTIP</dt> </dl>            | Combina el \_ \_ icono de TF LBI, TF \_ LBI \_ Text y TF \_ LBI \_ TOOLTIP.<br/>                                                                                                                                                                                                                                              |



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

[ITfLangBarItemSink:: actualización](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





