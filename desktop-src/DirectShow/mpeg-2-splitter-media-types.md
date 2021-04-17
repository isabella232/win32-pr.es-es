---
description: Tipos de medios de divisor MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de medios de divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689638"
---
# <a name="mpeg-2-splitter-media-types"></a>Tipos de medios de divisor MPEG-2

El filtro [de divisores MPEG-2](mpeg-2-splitter.md) admite actualmente audio y vídeo. Dolby AC-3 se admite como subflujo, tal y como se define en DVD. El filtro también admite audio MPEG-2. Los tipos de medios dependen de si el separador MPEG-2 está entregando paquetes PES o cargas de PES.

### <a name="video"></a>Vídeo

Para vídeo MPEG-2, los tipos de medios son los siguientes.



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | Salida de PES                               | Salida de carga                 |
| Tipo principal       | **\_PES MPEG2 \_ PE**                | **Vídeo de MEDIATYPE \_**           |
| Subtype          | **\_Vídeo MPEG2 de MEDIASUBTYPE \_**           | **\_Vídeo MPEG2 de MEDIASUBTYPE \_** |
| Tipo de formato      | **FORMATO \_ MPEG2Video**                   | **FORMATO \_ MPEG2Video**         |
| Estructura de formato | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>Audio AC-3

En el caso de audio AC-3, los tipos de medios son los siguientes.



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | Salida de PES                           | Salida de carga               |
| Tipo principal       | \_PES MPEG2 \_ PE                | **Audio de MEDIATYPE \_**         |
| Subtype          | MEDIASUBTYPE \_ Dolby \_ AC3             | **MEDIASUBTYPE \_ Dolby \_ AC3** |
| Tipo de formato      | DAR formato a \_ WaveFormatEx                 | **DAR formato a \_ WaveFormatEx**     |
| Estructura de formato | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

El miembro **wFormatTag** de la estructura **WAVEFORMATEX** para AC-3 es actualmente el **formato de onda \_ \_ desconocido**, pero esto podría cambiar.

### <a name="mpeg-2-audio"></a>Audio MPEG-2

En el caso de audio MPEG-2, los tipos de medios son los siguientes.



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | Salida de PES                    | Salida de carga                 |
| Tipo principal       | **\_PES MPEG2 \_ PE**     | **Audio de MEDIATYPE \_**           |
| Subtype          | **\_Audio MPEG2 de MEDIASUBTYE \_** | **\_Audio MPEG2 de MEDIASUBTYPE \_** |
| Tipo de formato      | **DAR formato a \_ WaveFormatEx**      | **DAR formato a \_ WaveFormatEx**       |
| Estructura de formato | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

El miembro **wFormatTag** de la estructura **WAVEFORMATEX** para audio MPEG-2 es actualmente el **formato de onda \_ \_ desconocido**, pero esto podría cambiar.

El separador MPEG-2 supone que las secuencias d0 a DF se usan para el flujo de extensión multicanal, ya que son para audio MPEG-2 de DVD. Por lo tanto, cada vez que se selecciona Stream C *x* , el divisor reenvía también los paquetes para Stream D *x* .

### <a name="lpcm-audio"></a>Audio LPCM

En el caso de audio LPCM, los tipos de medios son los siguientes.



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | Salida de PES                         | Salida de carga                     |
| Tipo principal       | **\_PES MPEG2 \_ PE**          | **Audio de MEDIATYPE \_**               |
| Subtype          | **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio** | **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio** |
| Tipo de formato      | **DAR formato a \_ WaveFormatEx**           | **DAR formato a \_ WaveFormatEx**           |
| Estructura de formato | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

Actualmente, el miembro **wFormatTag** de la estructura **WAVEFORMATEX** para audio LPCM es el **formato de onda \_ \_ desconocido**, pero esto podría cambiar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
