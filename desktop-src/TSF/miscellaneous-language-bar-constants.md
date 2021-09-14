---
title: Constantes de barra de lenguaje varios (Ctfutb.h)
description: Las constantes de la barra de idioma varias establecen ciertas propiedades de las barras de idioma.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361787"
---
# <a name="miscellaneous-language-bar-constants"></a>Constantes de barra de lenguaje varias

Las constantes de la barra de idioma varias establecen ciertas propiedades de las barras de idioma.



| Constante o valor                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <dt>**TF \_ DTLBI \_ USEPROFILEICON**</dt> <dt>0x00000001</dt> </dl> | El elemento de la barra de idioma del sistema debe mostrar el icono especificado para el perfil de idioma. Se usa en [los métodos ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) e [ITfSystemDeviceTypeLangBarItem::SetIconMode.](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)<br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <dt>**TF \_ INVALIDMENUITEM**</dt> <dt>(UINT)(-1)</dt> </dl>                 | No se utiliza.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <dt>**TF \_ LBI \_ BMPF \_ VERTICAL**</dt> <dt>0x00000001</dt> </dl>         | No se utiliza.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <dt>**TF \_ LBI \_ DESC \_ MAXLEN**</dt> <dt>32</dt> </dl>                       | Longitud, en caracteres WCHAR, del miembro de [estructura TF \_ LANGBARITEMINFO.szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).<br/>                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ctfutb.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctfutb.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





