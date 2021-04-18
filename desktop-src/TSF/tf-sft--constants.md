---
title: Constantes de TF_SFT_ (Ctfutb. h)
description: Las \_ \_ constantes de TF SFT \ especifican la configuración de presentación de una barra de idioma flotante.
ms.assetid: 628e1d85-9614-4327-b89b-723f6eeb0718
topic_type:
- apiref
api_name:
- TF_SFT_SHOWNORMAL
- TF_SFT_DOCK
- TF_SFT_MINIMIZED
- TF_SFT_HIDDEN
- TF_SFT_NOTRANSPARENCY
- TF_SFT_LOWTRANSPARENCY
- TF_SFT_HIGHTRANSPARENCY
- TF_SFT_LABELS
- TF_SFT_NOLABELS
- TF_SFT_EXTRAICONSONMINIMIZED
- TF_SFT_NOEXTRAICONSONMINIMIZED
- TF_SFT_DESKBAND
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a947960bfbe67585dc02a37de2da3dc6737540
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686003"
---
# <a name="tf_sft_-constants"></a>Constantes de TF \_ SFT \_ \*

Las constantes ** \_ TF \_ \* SFT* _ especifican la configuración de presentación de una barra de idioma flotante.



| Constante o valor                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <dt>_ * TF \_ SFT \_ SHOWNORMAL * *</dt> <dt>0x00000001</dt> </dl>                                        | Mostrar la barra de idioma como una ventana flotante. Esta constante no se puede combinar con las \_ constantes TF SFT \_ Dock, TF \_ SFT \_ Reduced, TF \_ SFT \_ Hidden o TF \_ SFT \_ DESKBAND.<br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <dt>**TF \_ SFT \_ Dock**</dt> <dt>0x00000002</dt> </dl>                                                          | Acople la barra de idioma en su propio panel de tareas. Esta constante no se puede combinar con las \_ constantes TF SFT \_ SHOWNORMAL, TF \_ SFT \_ minimizód, TF \_ SFT \_ Hidden o TF \_ SFT \_ DESKBAND. Solo disponible en Windows XP.<br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <dt>**TF \_ SFT \_ minimizado**</dt> <dt>0x00000004</dt> </dl>                                           | Mostrar la barra de idioma como un solo icono en la bandeja del sistema. Esta constante no se puede combinar con las \_ constantes TF SFT \_ SHOWNORMAL, TF \_ SFT \_ Dock, TF \_ SFT \_ Hidden o TF \_ SFT \_ DESKBAND. En Windows XP, use TF \_ SFT \_ DESKBAND en su lugar.<br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <dt>**TF \_ SFT \_ oculto**</dt> <dt>0x00000008</dt> </dl>                                                    | Oculte la barra de idioma. Esta constante no se puede combinar con las \_ constantes TF SFT \_ SHOWNORMAL, TF \_ SFT \_ Dock, TF \_ SFT \_ minimizód o TF \_ SFT \_ DESKBAND.<br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <dt>**TF \_ SFT \_ notransparency**</dt> <dt>0x00000010</dt> </dl>                            | Haga que la barra de idioma sea opaca.<br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <dt>**TF \_ SFT \_ LOWTRANSPARENCY**</dt> <dt>0x00000020</dt> </dl>                         | Haga que la barra de idioma sea parcialmente transparente. Solo disponible en Windows 2000 o posterior.<br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <dt>**TF \_ SFT \_ HIGHTRANSPARENCY**</dt> <dt>0x00000040</dt> </dl>                      | Haga que la barra de idioma sea muy transparente. Solo disponible en Windows 2000 o posterior.<br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <dt>**TF \_ \_Etiquetas de SFT**</dt> <dt>0x00000080</dt> </dl>                                                    | Mostrar etiquetas de texto junto a los iconos de la barra de idioma.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <dt>**TF \_ SFT \_ NOlabels**</dt> <dt>0x00000100</dt> </dl>                                              | Ocultar etiquetas de texto del icono de la barra de idioma.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <dt>**TF \_ SFT \_ EXTRAICONSONMINIMIZED**</dt> <dt>0x00000200</dt> </dl>       | Mostrar iconos de servicio de texto en la barra de tareas cuando se minimice la barra de idioma.<br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <dt>**TF \_ SFT \_ NOEXTRAICONSONMINIMIZED**</dt> <dt>0x00000400</dt> </dl> | Ocultar iconos de servicio de texto en la barra de tareas cuando la barra de idioma está minimizada.<br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <dt>**TF \_ SFT \_ DESKBAND**</dt> <dt>0x00000800</dt> </dl>                                              | Acople la barra de idioma en el extremo derecho de la barra de tareas del sistema (inmediatamente a la izquierda de la bandeja del sistema/reloj). Esta constante no se puede combinar con las \_ constantes TF SFT \_ SHOWNORMAL, TF \_ SFT \_ Dock, TF \_ SFT \_ minimizód o TF \_ SFT \_ Hidden. Solo disponible en Windows XP.<br/> |



## <a name="remarks"></a>Observaciones

El método [ITfLangBarMgr:: ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) establece el resultado de una operación **or** lógica en una o más de estas constantes para especificar los atributos del elemento de la barra de idioma.

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

[ITfLangBarMgr::ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 





