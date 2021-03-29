---
description: Se han definido varios subtipos para vídeo DV. Cada una tiene un código FOURCC y un valor GUID correspondiente. No se admiten todos estos formatos; Vea la sección Comentarios para obtener más información.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Subtipos de vídeo DV (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680735"
---
# <a name="dv-video-subtypes"></a>Subtipos de vídeo DV

Se han definido varios subtipos para vídeo DV. Cada una tiene un código FOURCC y un valor GUID correspondiente. No se admiten todos estos formatos; Vea la sección Comentarios para obtener más información.

## <a name="consumer-formats"></a>Formatos de consumidor



| FOURCC | GUID               | Velocidad de datos | Descripción                  |
|--------|--------------------|-----------|------------------------------|
| 'dvsl' | MEDIASUBTYPE \_ DVSL | 12,5 Mbps | SD-DVCR (525-60 o 625-50)   |
| 'dvsd' | MEDIASUBTYPE \_ DVSD | 25 Mbps   | SDL-DVCR (525-60 o 625-50)  |
| 'dvhd' | MEDIASUBTYPE \_ dvhd | 50 Mbps   | HD-DVCR (1125-60 o 1250-50) |



 

Consulte IEC-61834 para obtener más información acerca de estos formatos.

## <a name="professional-formats"></a>Formatos profesionales



| FOURCC | GUID               | Velocidad de datos | Descripción                                 |
|--------|--------------------|-----------|---------------------------------------------|
| 'dv25' | MEDIASUBTYPE \_ DV25 | 25 Mbps   | DVCPRO 25 (525-60 o 625-50).               |
| 'dv50' | MEDIASUBTYPE \_ DV50 | 50 Mbps   | DVCPRO 50 (525-60 o 625-50)                |
| 'dvh1' | MEDIASUBTYPE \_ dvh1 | 100 Mbps  | DVCPRO 100 (1080/60i, 1080/50i o 720/60P) |



 

Consulte SMPTE 314M para obtener más información sobre DV25 y DV50, y SMPTE 370M para obtener más información sobre dvh1.

## <a name="miscellaneous"></a>Varios

En el archivo de encabezado UUID. h se definen dos subtipos de DV adicionales. Estos se corresponden con los códigos FOURCC generados por determinados códecs DV; no se corresponden con ninguna de las normas DV definidas. Estos subtipos están obsoletos y no se deben usar.



| FOURCC | GUID               |
|--------|--------------------|
| DVCS | MEDIASUBTYPE \_ DVCS |
| 'DVSD' | MEDIASUBTYPE \_ DVSD |



 

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestran las tarifas de datos admitidas, en megabits por segundo (Mbps), para los controladores MSDV y UVC.



| Sistema operativo                                                                 | Controlador MSDV (IEEE 1394) | Controlador UVC    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| Windows XP Service Pack 1 o anterior                                             | 12,5, 25                | No disponible |
| Windows XP Service Pack 2 o posterior, Windows Server 2003 Service Pack 1 o posterior. | 12,5, 25, 50, 100       | 12,5, 25      |



 

En el caso de las secuencias de 25 Mbps, el comportamiento del controlador MSDV ha cambiado en Windows vista antes de Windows Vista, el controlador MSDV siempre establece el tipo de medio en MEDIASUBTYPE \_ DVSD para flujos de 25 Mbps, independientemente de si el origen es SDL-DVCR o DVCPRO 25. No se usó el tipo de medio ' DV25 '. A partir de Windows Vista, el controlador MSDV ahora distingue entre estos dos formatos. Para SDL-DVCR, sigue usando el subtipo "DVSD". En el caso de DVCPRO 25, ahora usa el subtipo ' DV25 '.

Los filtros de [divisor DV](dv-splitter-filter.md) de DirectShow y de [descodificador de vídeo DV](dv-video-decoder-filter.md) solo admiten los formatos SDL-DVCR. Los datos pueden ser PAL o NTSC. Pueden estar disponibles filtros o códecs de terceros que puedan analizar otros formatos DV, siempre que el controlador MSDV o UVC admita la velocidad de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Controlador MSDV](msdv-driver.md)
</dt> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> </dl>

 

 




