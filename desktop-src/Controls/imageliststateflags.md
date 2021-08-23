---
title: IMAGELISTSTATEFLAGS (Commctrl.h)
description: Las marcas siguientes se pasan al método IImageList Draw en el miembro fState de IMAGELISTDRAWPARAMS.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cbb4eef2f744c78e84999e9f07f3ca5a06d5dbf93dbfa26d5c6593d94d4e19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576145"
---
# <a name="imageliststateflags"></a>IMAGELISTSTATEFLAGS

Las marcas siguientes se pasan al método [**IImageList::D raw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) en el **miembro fState** de [**IMAGELISTDRAWPARAMS.**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)



| Constante o valor                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <dt>**ILS \_ Normal**</dt> <dt>0x00000000</dt> </dl>       | El estado de la imagen no se modifica.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <dt>**ILS \_ Glow**</dt> <dt>0x00000001</dt> </dl>             | No compatible. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <dt>**ILS \_ Shadow**</dt> <dt>0x00000002</dt> </dl>       | No compatible. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <dt>**ILS \_ SATURATE**</dt> <dt>0x00000004</dt> </dl> | Reduce la saturación de color del icono a escala de grises. Esto solo afecta a las imágenes de 32bpp. <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <dt>**ILS \_ Alpha**</dt> <dt>0x00000008</dt> </dl>          | Alfa combina el icono. La combinación alfa controla el nivel de transparencia de un icono, según el valor de su canal alfa. El valor del canal alfa se indica mediante el miembro **de marco** en el [**método IMAGELISTDRAWPARAMS.**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) El canal alfa puede estar entre 0 y 255, siendo 0 completamente transparente y 255 completamente opaco.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

