---
description: Se definen varios subtipos para vídeo DV. Cada uno tiene un código FOURCC y un valor GUID correspondiente. No se admiten todos estos formatos; vea la sección Comentarios para obtener más información.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Subtipos de vídeo DV (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246573"
---
# <a name="dv-video-subtypes"></a>Subtipos de vídeo DV

Se definen varios subtipos para vídeo DV. Cada uno tiene un código FOURCC y un valor GUID correspondiente. No se admiten todos estos formatos; vea la sección Comentarios para obtener más información.

## <a name="consumer-formats"></a>Formatos de consumidor



| FOURCC | GUID               | Velocidad de datos | Descripción                  |
|--------|--------------------|-----------|------------------------------|
| 'dvsl' | MEDIASUBTYPE \_ dvsl | 12,5 Mbps | SD-DVCR (525-60 o 625-50)   |
| 'dvsd' | MEDIASUBTYPE \_ dvsd | 25 Mbps   | SDL-DVCR (525-60 o 625-50)  |
| 'dvhd' | MEDIASUBTYPE \_ dvhd | 50 Mbps   | HD-DVCR (1125-60 o 1250-50) |



 

Consulte IEC-61834 para obtener más información sobre estos formatos.

## <a name="professional-formats"></a>Professional Formatos



| FOURCC | GUID               | Velocidad de datos | Descripción                                 |
|--------|--------------------|-----------|---------------------------------------------|
| 'dv25' | MEDIASUBTYPE \_ dv25 | 25 Mbps   | DVCPRO 25 (525-60 o 625-50).               |
| 'dv50' | MEDIASUBTYPE \_ dv50 | 50 Mbps   | DVCPRO 50 (525-60 o 625-50)                |
| 'dvh1' | MEDIASUBTYPE \_ dvh1 | 100 Mbps  | DVCPRO 100 (1080/60i, 1080/50i o 720/60P) |



 

Consulte SMPTE 314M para obtener más información sobre dv25 y dv50, y SMPTE 370M para obtener más información sobre dvh1.

## <a name="miscellaneous"></a>Varios

Se definen dos subtipos DV adicionales en el archivo de encabezado Uuids.h. Se corresponden con códigos FOURCC generados por determinados códecs DV; no se corresponden con ningún estándar DV definido. Estos subtipos están obsoletos y no se deben usar.



| FOURCC | GUID               |
|--------|--------------------|
| 'DVCS' | DVCS DE MEDIASUBTYPE \_ |
| 'DVSD' | MEDIASUBTYPE \_ DVSD |



 

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestran las velocidades de datos admitidas, en megabits por segundo (Mbps), para los controladores MSDV y UVC.



| Sistema operativo                                                                 | Controlador MSDV (IEEE 1394) | Controlador UVC    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| Windows XP Service Pack 1 o anterior                                             | 12.5, 25                | No disponible |
| Windows XP Service Pack 2 o posterior, Windows Server 2003 Service Pack 1 o posterior. | 12.5, 25, 50, 100       | 12.5, 25      |



 

Para secuencias de 25 Mbps, el comportamiento del controlador MSDV ha cambiado en Windows Vista Antes de Windows Vista, el controlador MSDV siempre establece el tipo de medio en MEDIASUBTYPE dvsd para secuencias de 25 Mbps, independientemente de si el origen era \_ SDL-DVCR o DVCPRO 25. No se usó el tipo de medio "dv25". A partir Windows Vista, el controlador MSDV ahora distingue entre estos dos formatos. Para SDL-DVCR, sigue utilizando el subtipo "dvsd". Para DVCPRO 25, ahora usa el subtipo "dv25".

Los DirectShow [divisor DV y](dv-splitter-filter.md) descodificador de vídeo [DV](dv-video-decoder-filter.md) solo admiten formatos SDL-DVCR. Los datos pueden ser PAL o ÁLISIS. Es posible que haya filtros o códecs de terceros disponibles que puedan analizar otros formatos DV, siempre y cuando la velocidad de datos sea compatible con el controlador MSDV o UVC.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Controlador MSDV](msdv-driver.md)
</dt> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> </dl>

 

 




