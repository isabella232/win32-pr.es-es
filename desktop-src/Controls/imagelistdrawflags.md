---
title: IMAGELISTDRAWFLAGS (commctrl. h)
description: Se pasa al método draw IImageList en el miembro fStyle de IMAGELISTDRAWPARAMS.
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
ms.openlocfilehash: 0743fc2778b3ef693646327fe8206ebedcb89e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996217"
---
# <a name="imagelistdrawflags"></a>IMAGELISTDRAWFLAGS

Se pasa al método [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) en el miembro **fStyle** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Constante o valor                                                                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**Rar \_ NORMAL**</dt> <dt>0x00000000</dt> </dl>                      | Dibuja la imagen con el color de fondo de la lista de imágenes. Si el color de fondo es el \_ valor NONE de CLR, la imagen se dibuja de forma transparente con la máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**Rar \_ TRANSPARENTE**</dt> <dt>0x00000001</dt> </dl>       | Dibuja la imagen de forma transparente con la máscara, independientemente del color de fondo. Este valor no tiene ningún efecto si la lista de imágenes no contiene una máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**Rar \_ BLEND25**</dt> <dt>0x00000002</dt> </dl>                   | Dibuja la imagen y combina el 25 por ciento con el color de fusión especificado por **rgbFg**. Este valor no tiene ningún efecto si la lista de imágenes no contiene una máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**Rar \_ FOCO**</dt> <dt>0x00000002</dt> </dl>                         | Igual que **rar \_ BLEND25**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**Rar \_ BLEND50**</dt> <dt>0x00000004</dt> </dl>                   | Dibuja la imagen y combina el 50 por ciento con el color de fusión especificado por **rgbFg**. Este valor no tiene ningún efecto si la lista de imágenes no contiene una máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**Rar \_ SELECCIONADO**</dt> <dt>0x00000004</dt> </dl>                | Igual que **rar \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**Rar \_ BLEND**</dt> <dt>0x00000004</dt> </dl>                         | Igual que **rar \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**Rar \_ MÁSCARA**</dt> <dt>0x00000010</dt> </dl>                            | Dibuja la máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**Rar \_ IMAGEN**</dt> <dt>0x00000020</dt> </dl>                         | Si la superposición no requiere que se dibuje una máscara, establezca esta marca.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**Rar \_**</dt> <dt>0x00000040</dt> ROP </dl>                               | Dibuja la imagen mediante el código de operación de trama especificado por el miembro **dwRop** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**Rar \_ OVERLAYMASK**</dt> <dt>0x00000F00</dt> </dl>       | Para extraer la imagen de superposición del miembro **fStyle** , use el operador lógico and para combinar **fStyle** con el valor de **rar \_ OVERLAYMASK** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**Rar \_ PRESERVEALPHA**</dt> <dt>0x00001000</dt> </dl> | Conserva el canal alfa en el destino.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**Rar \_ SCALE**</dt> <dt>0x00002000</dt> </dl>                         | Hace que la imagen se escale a CX, CY en lugar de recortarse.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**Rar \_ DPISCALE**</dt> <dt>0x00004000</dt> </dl>                | Escala la imagen a los PPP actuales de la pantalla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**Rar \_ ASYNC**</dt> <dt>0x00008000</dt> </dl>                         | **Windows Vista y versiones posteriores.** Dibuje la imagen si está disponible en la memoria caché. No lo extraiga automáticamente. El método draw llamado devuelve E \_ pendiente al componente que realiza la llamada, que, a continuación, debe realizar una acción alternativa, como, proporcionar otra imagen y poner en cola una tarea en segundo plano para forzar la carga de la imagen a través de [**ForceImagePresent**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) con la marca de ILFIP \_ Always. La \_ marca ASINCRÓNICA rar impide que la operación de extracción bloquee el subproceso actual y es especialmente importante si se llama a un método draw desde el subproceso de la interfaz de usuario (IU).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

