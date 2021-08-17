---
title: TF_LBI_STYLE_ constantes (Ctfutb.h)
description: Las constantes STYLE \ de TF LBI se usan en el miembro dwStyle de la estructura \_ \_ \_ LANGBARITEMINFO de TF para especificar el estilo de un \_ elemento de la barra de lenguaje.
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
ms.openlocfilehash: 9954c416d9ad28f0ba0b2ddd6853b125039bf4db24adb3b3ff41f8722b2ba494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950800"
---
# <a name="tf_lbi_style_-constants"></a>Constantes \_ TF LBI \_ STYLE \_ \*

Las constantes STYLE _ de TF LBI se usan en el **\_ miembro \_ \_ \* *_* dwStyle** de la estructura [ \_ LANGBARITEMINFO de TF](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo) para especificar el estilo de un elemento de la barra de lenguaje.

Si este estilo se combina con TF \_ LBI \_ STYLE \_ BTN BUTTON, se mostrará una flecha desplegable para el elemento además \_ del texto. La flecha desplegable funciona como el botón de menú y, al hacer clic en él, se llamará a **ITfLangBarItemButton::InitMenu.** Al hacer clic en la parte de texto del botón, se llamará a **ITfLangBarItemButton::OnClick.**



| Constante o valor                                                                                                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**TF \_ Estilo LBI \_ \_ HIDDENSTATUSCONTROL**</dt> <dt>0x00000001</dt> </dl> | El elemento se puede ocultar o mostrar dinámicamente mediante el valor DE TF LBI STATUS HIDDEN en el \_ \_ método \_ [ITfLangBarItem::GetStatus.](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) Si este valor no está presente, el elemento no se puede ocultar de esta manera.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**TF \_ ESTILO LBI \_ \_ MOSTRADOINTRAY**</dt> <dt>0x00000002</dt> </dl>                         | El elemento se mostrará en la bandeja de iconos de notificación además de la barra de idioma. Esta marca no se admite actualmente.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**TF \_ LBI \_ STYLE \_ HIDEONNOOTHERITEMS**</dt> <dt>0x00000004</dt> </dl>    | La barra de idioma está oculta si todos los elementos de la barra de idioma contienen este estilo. Si algún elemento de la barra de idioma no contiene este estilo, se muestra la barra de idioma.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**TF \_ ESTILO LBI \_ \_ MOSTRADOINTRAYONLY**</dt> <dt>0x00000008</dt> </dl>             | El elemento solo se mostrará en la bandeja de iconos de notificación y no en la barra de idioma. Esta marca no se admite actualmente.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**TF \_ ESTILO LBI \_ \_ HIDDENBYDEFAULT**</dt> <dt>0x00000010</dt> </dl>             | El elemento no se muestra en la barra de herramientas hasta que se selecciona en el menú de opciones de la barra de idioma. Esta marca se omite si está establecido EL CONTROL HIDDENSTATUSCONTROL DE ESTILO LBI de TF o el usuario ya ha cambiado el estado oculto o mostrado mediante el menú de opciones de la barra \_ \_ de \_ idioma.<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**TF \_ \_ \_ TEXTCOLORICON DE ESTILO LBI**</dt> <dt>0x00000020</dt> </dl>                   | Cualquier píxel negro dentro del icono se convertirá al color del texto del tema seleccionado. El icono debe ser monocromo.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**TF \_ Botón \_ \_ BTN \_ DE**</dt> ESTILO LBI <dt>0x00010000</dt> </dl>                           | El elemento es un botón de inserción. [Se llama a ITfLangBarItemButton::OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) cuando se presiona el elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**TF \_ Menú \_ \_ BTN \_ DE**</dt> ESTILO LBI <dt>0x00020000</dt> </dl>                                 | El elemento es un menú. [Se llama a ITfLangBarItemButton::InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) cuando se presiona el elemento.<br/> Si este estilo se combina con TF \_ LBI \_ STYLE \_ BTN BUTTON, se mostrará una flecha desplegable para el elemento además \_ del texto. La flecha desplegable funciona como el botón de menú y, al hacer clic en él, se llamará a **ITfLangBarItemButton::InitMenu.** Al hacer clic en la parte de texto del botón, se llamará a **ITfLangBarItemButton::OnClick.**<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**TF \_ Botón de \_ alternancia \_ BTN \_ DE**</dt> ESTILO LBI <dt>0x00040000</dt> </dl>                           | El elemento es un botón de alternancia y funciona de forma similar a una casilla. **Se llama a ITfLangBarItemButton::OnClick** cuando se presiona el elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>Ctfutb.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITfLangBarItem::GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





