---
title: Marcas de creación de listas de imágenes (Shlobj.h)
description: Conjunto de marcas de bits que especifica el tipo de lista de imágenes que se creará. Este parámetro puede ser una combinación de los siguientes valores, pero solo puede incluir uno de los valores de COLOR de \_ ILC. Usado por ImageList \_ Create e IImageList2 Initialize.
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
ms.openlocfilehash: ac1197604750e5da9248200b2dbcf37e53611d83842a401aafc3d2ded70c9179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958694"
---
# <a name="image-list-creation-flags"></a>Marcas de creación de listas de imágenes

Conjunto de marcas de bits que especifica el tipo de lista de imágenes que se creará. Este parámetro puede ser una combinación de los siguientes valores, pero solo puede incluir uno de los valores de COLOR de \_ ILC. Usado por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) e [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).



| Constante o valor                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**ILC \_ Mask**</dt> <dt>0x00000001</dt> </dl>                                     | Use una máscara. La lista de imágenes contiene dos mapas de bits, uno de los cuales es un mapa de bits monocromático que se usa como máscara. Si no se incluye este valor, la lista de imágenes solo contiene un mapa de bits.<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**ILC \_ Color**</dt> <dt>0x00000000</dt> </dl>                                  | Use el comportamiento predeterminado si no se especifica ninguna de las \_ otras marcas COLORx de ILC. Normalmente, el valor predeterminado es ILC COLOR4, pero para los controladores de pantalla más antiguos, el valor predeterminado \_ es ILC \_ COLORDDB.<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**ILC \_ ColorDDB**</dt> <dt>0x000000FE</dt> </dl>                         | Use un mapa de bits dependiente del dispositivo.<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**ILC \_ Color4**</dt> <dt>0x00000004</dt> </dl>                               | Use una sección de mapa de bits independiente del dispositivo (DIB) de 4 bits (16 colores) como mapa de bits de la lista de imágenes.<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**ILC \_ Color8**</dt> <dt>0x00000008</dt> </dl>                               | Use una sección DIB de 8 bits. Los colores usados para la tabla de colores son los mismos que la paleta de semitonos.<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**ILC \_ Color16**</dt> <dt>0x00000010</dt> </dl>                            | Use una sección DIB de 16 bits (color de 32/64 k).<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**ILC \_ Color24**</dt> <dt>0x00000018</dt> </dl>                            | Use una sección DIB de 24 bits.<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**ILC \_ Color32**</dt> <dt>0x00000020</dt> </dl>                            | Use una sección DIB de 32 bits.<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**ILC \_ Paleta**</dt> <dt>0x00000800</dt> </dl>                            | Sin implementar.<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**ILC \_ Mirror**</dt> <dt>0x00002000</dt> </dl>                               | Reflejar los iconos contenidos, si el proceso está reflejado<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**ILC \_ PERITEMMIRROR**</dt> <dt>0x00008000</dt> </dl>          | Hace que el código de creación de reflejo refleja cada elemento al insertar un conjunto de imágenes, frente a toda la franja.<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**ILC \_ OriginalSIZE**</dt> <dt>0x00010000</dt> </dl>             | **Windows Vista y versiones posteriores.** Imagelist debe aceptar imágenes más pequeñas que establecidas y aplicar el tamaño original en función de la imagen agregada.<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**ILC \_ HighQUALITYSCALE**</dt> <dt>0x00020000</dt> </dl> | **Windows Vista y versiones posteriores.** Reservado.<br/>                                                                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 





