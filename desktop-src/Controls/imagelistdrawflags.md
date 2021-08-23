---
title: IMAGELISTDRAWFLAGS (Commctrl.h)
description: Se pasa al método IImageList Draw en el miembro fStyle de IMAGELISTDRAWPARAMS.
ms.assetid: 99fd2cb2-0cb0-40c2-b184-b6d8e54397b4
topic_type:
- apiref
api_name:
- ILD_NORMAL
- ILD_TRANSPARENT
- ILD_BLEND25
- ILD_FOCUS
- ILD_BLEND50
- ILD_SELECTED
- ILD_BLEND
- ILD_MASK
- ILD_IMAGE
- ILD_ROP
- ILD_OVERLAYMASK
- ILD_PRESERVEALPHA
- ILD_SCALE
- ILD_DPISCALE
- ILD_ASYNC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e44d863e82cf126c62262a564e5bf8366fbe71dbb75cc6d47bd16634d798cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544545"
---
# <a name="imagelistdrawflags"></a>IMAGELISTDRAWFLAGS

Se pasa [**al método IImageList::D raw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) en el **miembro fStyle** de [**IMAGELISTDRAWPARAMS.**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams)



| Constante o valor                                                                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**ILD \_ Normal**</dt> <dt>0x00000000</dt> </dl>                      | Dibuja la imagen con el color de fondo de la lista de imágenes. Si el color de fondo es el valor \_ NONE de CLR, la imagen se dibuja de forma transparente mediante la máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**ILD \_ Transparente**</dt> <dt>0x00000001</dt> </dl>       | Dibuja la imagen de forma transparente mediante la máscara, independientemente del color de fondo. Este valor no tiene ningún efecto si la lista de imágenes no contiene una máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**ILD \_ Blend25**</dt> <dt>0x00000002</dt> </dl>                   | Dibuja la imagen, mezclando el 25 por ciento con el color de mezcla especificado por **rgbFg**. Este valor no tiene ningún efecto si la lista de imágenes no contiene una máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**ILD \_ Enfoque**</dt> <dt>0x00000002</dt> </dl>                         | Igual que **ILD \_ BLEND25.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**ILD \_ Blend50**</dt> <dt>0x00000004</dt> </dl>                   | Dibuja la imagen, mezclando el 50 por ciento con el color de mezcla especificado por **rgbFg**. Este valor no tiene ningún efecto si la lista de imágenes no contiene una máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**ILD \_ SELECCIÓN**</dt> <dt>0X00000004</dt> </dl>                | Igual que **ILD \_ BLEND50.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**ILD \_ BLEND**</dt> <dt>0x00000004</dt> </dl>                         | Igual que **ILD \_ BLEND50.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**ILD \_ Mask**</dt> <dt>0x00000010</dt> </dl>                            | Dibuja la máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**ILD \_ Image**</dt> <dt>0x00000020</dt> </dl>                         | Si la superposición no requiere que se dibujara una máscara, establezca esta marca.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**ILD \_ Rop**</dt> <dt>0x00000040</dt> </dl>                               | Dibuja la imagen mediante el código de operación de trama especificado por el **miembro dwRop.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**ILD \_ OVERLAYMASK**</dt> <dt>0x00000F00</dt> </dl>       | Para extraer la imagen superpuesta del **miembro fStyle,** use el and lógico para combinar **fStyle** con el **valor DE ILD \_ OVERLAYMASK.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**ILD \_ PRESERVEALPHA**</dt> <dt>0x00001000</dt> </dl> | Conserva el canal alfa en el destino.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**ILD \_ Escalado**</dt> <dt>0x00002000</dt> </dl>                         | Hace que la imagen se escale a cx, cy en lugar de recortarse.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**ILD \_ Valores de PPPSCALE**</dt> <dt>0x00004000</dt> </dl>                | Escala la imagen a los ppp actuales de la pantalla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**ILD \_ ASYNC**</dt> <dt>0x00008000</dt> </dl>                         | **Windows Vista y versiones posteriores.** Dibuje la imagen si está disponible en la memoria caché. No lo extraiga automáticamente. El método draw llamado devuelve E PENDING al componente de llamada, que debe realizar una acción alternativa, como proporcionar otra imagen y poner en cola una tarea en segundo plano para forzar la carga de la imagen a través de ForceImagePresent mediante la marca \_ ILFIP [](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) \_ ALWAYS. A continuación, la marca ILD ASYNC impide que la operación de extracción bloquee el subproceso actual y es especialmente importante si se llama a un método draw desde el subproceso de la interfaz de \_ usuario (UI).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

