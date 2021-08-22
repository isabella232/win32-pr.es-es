---
title: TF_SFT_ constantes (Ctfutb.h)
description: Las constantes \_ de TF SFT \_ \ especifican la configuración de presentación de una barra de lenguaje flotante.
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
ms.openlocfilehash: d8d318e2bc9b1f233d6d1cc8210d380f91d881178d20a334f2612d0e12563e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118874218"
---
# <a name="tf_sft_-constants"></a>Constantes \_ de TF SFT \_ \*

Las **constantes de TF \_ SFT \_ \*** especifican la configuración de presentación de una barra de lenguaje flotante.



| Constante o valor                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <dt>**TF \_ SFT \_ SHOWNORMAL**</dt> <dt>0x00000001</dt> </dl>                                        | Muestra la barra de idioma como una ventana flotante. Esta constante no se puede combinar con las constantes TF \_ SFT \_ DOCK, TF \_ SFT \_ MINIMIZED, TF SFT HIDDEN o \_ \_ TF \_ SFT \_ DESKBAND.<br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <dt>**TF \_ SFT \_ DOCK**</dt> <dt>0x00000002</dt> </dl>                                                          | Acoplar la barra de idioma en su propio panel de tareas. Esta constante no se puede combinar con las constantes \_ TF SFT \_ SHOWNORMAL, TF \_ SFT \_ MINIMIZED, TF SFT HIDDEN o \_ \_ TF \_ SFT \_ DESKBAND. Disponible solo en Windows XP.<br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <dt>**TF \_ SFT \_ MINIMIZADO**</dt> <dt>0x00000004</dt> </dl>                                           | Muestre la barra de idioma como un único icono en la bandeja del sistema. Esta constante no se puede combinar con las constantes \_ TF SFT \_ SHOWNORMAL, TF \_ SFT \_ DOCK, TF SFT HIDDEN o TF \_ \_ \_ SFT \_ DESKBAND. En Windows XP, use TF \_ SFT \_ DESKBAND en su lugar.<br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <dt>**TF \_ SFT \_ HIDDEN**</dt> <dt>0x00000008</dt> </dl>                                                    | Oculte la barra de idioma. Esta constante no se puede combinar con las constantes \_ TF SFT \_ SHOWNORMAL, TF \_ SFT \_ DOCK, TF \_ SFT MINIMIZED o TF \_ \_ SFT \_ DESKBAND.<br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <dt>**TF \_ SFT \_ NOTRANSPARENCY**</dt> <dt>0x00000010</dt> </dl>                            | Haga que la barra de idioma sea opaca.<br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <dt>**TF \_ SFT \_ LOWTRANSPARENCY**</dt> <dt>0x00000020</dt> </dl>                         | Haga que la barra de idioma sea parcialmente transparente. Disponible solo en Windows 2000 o posterior.<br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <dt>**TF \_ SFT \_ HIGHTRANSPARENCY**</dt> <dt>0x00000040</dt> </dl>                      | Haga que la barra de idioma sea muy transparente. Disponible solo en Windows 2000 o posterior.<br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <dt>**TF \_ Etiquetas \_ SFT**</dt> <dt>0x00000080</dt> </dl>                                                    | Mostrar etiquetas de texto junto a los iconos de la barra de idioma.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <dt>**TF \_ SFT \_ NOLABELS**</dt> <dt>0x00000100</dt> </dl>                                              | Ocultar etiquetas de texto del icono de la barra de idioma.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <dt>**TF \_ SFT \_ EXTRAICOMINIMIZED**</dt> <dt>0x00000200</dt> </dl>       | Mostrar iconos de servicio de texto en la barra de tareas cuando se minimiza la barra de idioma.<br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <dt>**TF \_ SFT \_ NOEXTRAICOMINIMIZED**</dt> <dt>0x00000400</dt> </dl> | Oculte los iconos del servicio de texto en la barra de tareas cuando se minimice la barra de idioma.<br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <dt>**TF \_ SFT \_ DESKBAND**</dt> <dt>0x00000800</dt> </dl>                                              | Acoplar la barra de idioma en el extremo derecho de la barra de tareas del sistema (inmediatamente a la izquierda de la bandeja o el reloj del sistema). Esta constante no se puede combinar con las constantes \_ TF SFT \_ SHOWNORMAL, TF \_ SFT \_ DOCK, TF \_ SFT MINIMIZED o TF \_ \_ SFT \_ HIDDEN. Disponible solo en Windows XP.<br/> |



## <a name="remarks"></a>Comentarios

El [método ITfLangBarMgr::ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) establece el resultado de una operación **OR** lógica en una o varias de estas constantes para especificar los atributos del elemento de la barra de lenguaje.

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

[ITfLangBarMgr::ShowFloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 





