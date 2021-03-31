---
title: Constantes de TF_LBI_STYLE_ (Ctfutb. h)
description: Las constantes de TF \_ LBI \_ style \_ \ se usan en el miembro dwStyle de la \_ estructura TF LANGBARITEMINFO para especificar el estilo de un elemento de la barra de idioma.
ms.assetid: 9180a666-774f-401b-bea3-68d5396fab30
topic_type:
- apiref
api_name:
- TF_LBI_STYLE_HIDDENSTATUSCONTROL
- TF_LBI_STYLE_SHOWNINTRAY
- TF_LBI_STYLE_HIDEONNOOTHERITEMS
- TF_LBI_STYLE_SHOWNINTRAYONLY
- TF_LBI_STYLE_HIDDENBYDEFAULT
- TF_LBI_STYLE_TEXTCOLORICON
- TF_LBI_STYLE_BTN_BUTTON
- TF_LBI_STYLE_BTN_MENU
- TF_LBI_STYLE_BTN_TOGGLE
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b43ef805161afce6cb73bfaa26060308bc0aa5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490462"
---
# <a name="tf_lbi_style_-constants"></a>Constantes de estilo de la TF \_ LBI \_ \_ \*

Las **constantes de tipo de la opción TF \_ LBI \_ \_ \* *se usan en el miembro _* dwStyle** de la estructura [TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo) para especificar el estilo de un elemento de la barra de idioma.

Si este estilo se combina con el \_ botón de TF LBI \_ estilo \_ BTN \_ , se mostrará una flecha de lista desplegable para el elemento además del texto. La flecha desplegable funciona como el botón de menú y, al hacer clic en ella, se llamará a **ITfLangBarItemButton:: InitMenu** . Al hacer clic en la parte de texto del botón, se llamará a **ITfLangBarItemButton:: OnClick** .



| Constante o valor                                                                                                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**TF \_ \_Estilo LBI \_ HIDDENSTATUSCONTROL**</dt> <dt>0x00000001</dt> </dl> | El elemento se puede ocultar o mostrar de forma dinámica mediante el \_ \_ valor de TF LBI status \_ Hidden en el método [ITfLangBarItem:: getStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) . Si este valor no está presente, el elemento no se puede ocultar de esta manera.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**TF \_ \_Estilo LBI \_ SHOWNINTRAY**</dt> <dt>0x00000002</dt> </dl>                         | El elemento se mostrará en la bandeja del icono de notificación, además de en la barra de idioma. Esta marca no se admite actualmente.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**TF \_ \_Estilo LBI \_ HIDEONNOOTHERITEMS**</dt> <dt>0x00000004</dt> </dl>    | La barra de idioma está oculta si todos los elementos de la barra de idioma contienen este estilo. Si algún elemento de la barra de idioma no contiene este estilo, se muestra la barra de idioma.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**TF \_ \_Estilo LBI \_ SHOWNINTRAYONLY**</dt> <dt>0x00000008</dt> </dl>             | El elemento solo se mostrará en la bandeja del icono de notificación y no en la barra de idioma. Esta marca no se admite actualmente.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**TF \_ \_Estilo LBI \_ HIDDENBYDEFAULT**</dt> <dt>0x00000010</dt> </dl>             | El elemento no se muestra en la barra de herramientas hasta que se selecciona en el menú de opciones de la barra de idioma. Esta marca se omite si \_ se establece el valor de TF LBI \_ style \_ HIDDENSTATUSCONTROL o si el usuario ya ha cambiado el estado oculto o mostrado mediante el menú de opciones de la barra de idioma.<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**TF \_ \_Estilo LBI \_ TEXTCOLORICON**</dt> <dt>0x00000020</dt> </dl>                   | Los píxeles negros del icono se convertirán al color del texto del tema seleccionado. El icono debe ser monocromo.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**TF \_ \_ \_ \_ Botón BTN de estilo LBI**</dt> <dt>0x00010000</dt> </dl>                           | El elemento es un botón de reenvío. Se llama a [ITfLangBarItemButton:: OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) cuando se presiona el elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**TF \_ \_Estilo LBI \_ 0x00020000 \_ menú BTN**</dt> <dt></dt> </dl>                                 | El elemento es un menú. Se llama a [ITfLangBarItemButton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) cuando se presiona el elemento.<br/> Si este estilo se combina con el \_ botón de TF LBI \_ estilo \_ BTN \_ , se mostrará una flecha de lista desplegable para el elemento además del texto. La flecha desplegable funciona como el botón de menú y, al hacer clic en ella, se llamará a **ITfLangBarItemButton:: InitMenu** . Al hacer clic en la parte de texto del botón, se llamará a **ITfLangBarItemButton:: OnClick** .<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**TF \_ Estilo LBI comando \_ \_ BTN \_ Toggle**</dt> <dt></dt> </dl>                           | El elemento es un botón de alternancia y funciona de forma similar a una casilla. Se llama a **ITfLangBarItemButton:: OnClick** cuando se presiona el elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                       |



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

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITfLangBarItem:: GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





