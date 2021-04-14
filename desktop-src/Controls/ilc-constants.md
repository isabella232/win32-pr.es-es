---
title: Marcas de creación de la lista de imágenes (ShlObj. h)
description: Conjunto de marcadores de bits que especifica el tipo de lista de imágenes que se va a crear. Este parámetro puede ser una combinación de los valores siguientes, pero solo puede incluir uno de los valores de \_ color ILC. Lo usan ImageList \_ Create y IImageList2 Initialize.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490210"
---
# <a name="image-list-creation-flags"></a>Marcas de creación de lista de imágenes

Conjunto de marcadores de bits que especifica el tipo de lista de imágenes que se va a crear. Este parámetro puede ser una combinación de los valores siguientes, pero solo puede incluir uno de los valores de \_ color ILC. Usado por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) y [**IImageList2:: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).



| Constante o valor                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**ILC \_ MÁSCARA**</dt> <dt>0x00000001</dt> </dl>                                     | Use una máscara. La lista de imágenes contiene dos mapas de bits, uno de los cuales es un mapa de bits monocromo que se usa como máscara. Si no se incluye este valor, la lista de imágenes solo contiene un mapa de bits.<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**ILC \_ COLOR**</dt> <dt>0x00000000</dt> </dl>                                  | Use el comportamiento predeterminado si no se especifica ninguna de las otras marcas de ILC \_ COLORx. Normalmente, el valor predeterminado es ILC \_ COLOR4, pero para los controladores de pantalla anteriores, el valor predeterminado es ILC \_ COLORDDB.<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**ILC \_ COLORDDB**</dt> <dt>0x000000FE</dt> </dl>                         | Use un mapa de bits dependiente del dispositivo.<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt> </dl>                               | Use una sección de mapa de bits independiente del dispositivo (DIB) de 4 bits (16 colores) como mapa de bits para la lista de imágenes.<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt> </dl>                               | Use una sección DIB de 8 bits. Los colores usados para la tabla de colores son los mismos que los colores de la paleta de semitonos.<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt> </dl>                            | Use una sección DIB de 16 bits (32/64k-color).<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt> </dl>                            | Use una sección DIB de 24 bits.<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt> </dl>                            | Use una sección DIB de 32 bits.<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**ILC \_ PALETA**</dt> <dt>0x00000800</dt> </dl>                            | Sin implementar.<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**ILC \_**</dt> <dt></dt> Recreativo de reflejo </dl>                               | Reflejar los iconos contenidos, si el proceso está reflejado<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**ILC \_ PERITEMMIRROR**</dt> <dt>0x00008000</dt> </dl>          | Hace que el código de creación de reflejo refleje cada elemento al insertar un conjunto de imágenes, en lugar de toda la franja.<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**ILC \_ ORIGINALSIZE**</dt> <dt>0x00010000</dt> </dl>             | **Windows Vista y versiones posteriores.** ImageList debe aceptar menor que las imágenes establecidas y aplicar el tamaño original en función de la imagen agregada.<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**ILC \_ HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt> </dl> | **Windows Vista y versiones posteriores.** Reservado.<br/>                                                                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 





