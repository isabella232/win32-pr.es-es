---
title: IMAGELISTSTATEFLAGS (commctrl. h)
description: Las marcas siguientes se pasan al método draw IImageList en el miembro fState de IMAGELISTDRAWPARAMS.
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
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079207"
---
# <a name="imageliststateflags"></a>IMAGELISTSTATEFLAGS

Las marcas siguientes se pasan al método [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) en el miembro **fState** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Constante o valor                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <dt>**ILS \_ NORMAL**</dt> <dt>0x00000000</dt> </dl>       | El estado de la imagen no se ha modificado.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <dt>**ILS \_ RESPLANDOR**</dt> <dt>0x00000001</dt> </dl>             | No se admite. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <dt>**ILS \_ SOMBRA**</dt> <dt>0x00000002</dt> </dl>       | No se admite. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <dt>**ILS \_ SATURAr**</dt> <dt>0x00000004</dt> </dl> | Reduce la saturación de color del icono a escala de grises. Esto solo afecta a las imágenes de 32 bpp. <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <dt>**ILS \_ ALFA**</dt> <dt>0x00000008</dt> </dl>          | Alfa combina el icono. La combinación alfa controla el nivel de transparencia de un icono, según el valor de su canal alfa. El valor del canal alfa se indica mediante el miembro de **marco** en el método [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) . El canal alfa puede estar comprendido entre 0 y 255, donde 0 es completamente transparente y 255 es totalmente opaco.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

