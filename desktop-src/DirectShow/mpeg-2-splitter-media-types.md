---
description: Tipos de medios divisores MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipos de medios divisores MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119980"
---
# <a name="mpeg-2-splitter-media-types"></a>Tipos de medios divisores MPEG-2

El [filtro divisor MPEG-2](mpeg-2-splitter.md) admite actualmente audio y vídeo. Dolby AC-3 se admite como una subtransmisión, tal y como se define en DVD. El filtro también admite audio MPEG-2. Los tipos de medios dependen de si el divisor MPEG-2 entrega paquetes PES o cargas PES.

### <a name="video"></a>Vídeo

En el caso del vídeo MPEG-2, los tipos de medios son los siguientes.


|                | Salida de PES | Salida de carga
|------------------|------------------------------------------|--------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **Vídeo \_ DE MEDIATYPE**           |
| **Subtipo**          | **VÍDEO MPEG2 DE MEDIASUBTYPE \_ \_**           | **VÍDEO MPEG2 DE MEDIASUBTYPE \_ \_** |
| **Tipo de formato**      | **FORMAT \_ MPEG2Video**                   | **FORMAT \_ MPEG2Video**         |
| **Estructura de formato** | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>AC-3 Audio

Para el audio AC-3, los tipos de medios son los siguientes.

| | Salida de PES | Salida de carga |
|------------------|--------------------------------------|------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **MEDIATYPE \_ Audio**         |
| **Subtipo**          | **MEDIASUBTYPE \_ DOLBY \_ AC3**             | **MEDIASUBTYPE \_ DOLBY \_ AC3** |
| **Tipo de formato**      | FORMAT \_ WaveFormatEx                 | **FORMAT \_ WaveFormatEx**     |
| **Estructura de formato** | [**FORMA DE ONDAATEX**](/previous-versions/dd757713(v=vs.85)) | **FORMA DE ONDAATEX**             |



 

El miembro **wFormatTag** de la estructura **WAVEATEX** para AC-3 es actualmente **WAVE FORMAT \_ \_ UNKNOWN,** pero esto podría cambiar.

### <a name="mpeg-2-audio"></a>MPEG-2 Audio

En el caso del audio MPEG-2, los tipos de medios son los siguientes.



|  | Salida de PES | Salida de carga |
|------------------|-------------------------------|--------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**     | **MEDIATYPE \_ Audio**           |
| **Subtipo**          | **AUDIO MPEG2 DE MEDIASUBTYE \_ \_** | **MEDIASUBTYPE \_ MPEG2 \_ AUDIO** |
| **Tipo de formato**      | **FORMAT \_ WaveFormatEx**      | **FORMAT \_ WaveFormatEx**       |
| **Estructura de formato** | **FORMA DE ONDAATEX**              | **FORMA DE ONDAATEX**               |



 

El miembro **wFormatTag** de la estructura **WAVEATEX** para MPEG-2 Audio es actualmente **WAVE FORMAT \_ \_ UNKNOWN,** pero esto podría cambiar.

El divisor MPEG-2 supone que las secuencias D0 a DF se usan para la secuencia de extensión multicanal, como para el audio MPEG-2 de DVD. Por lo tanto, cada vez que se selecciona la secuencia C *x,* el divisor reenvía también los paquetes para la secuencia D *x.*

### <a name="lpcm-audio"></a>LPCM Audio

En el caso del audio LPCM, los tipos de medios son los siguientes.



|  | Salida de PES | Salida de carga |
|------------------|------------------------------------|------------------------------------|
| **Tipo principal**       | **MEDIATYPE \_ MPEG2 \_ PES**          | **MEDIATYPE \_ Audio**               |
| **Subtipo**          | **AUDIO \_ LPCM de DVD DE MEDIASUBTYPE \_ \_** | **AUDIO \_ LPCM de DVD DE MEDIASUBTYPE \_ \_** |
| **Tipo de formato**      | **FORMAT \_ WaveFormatEx**           | **FORMAT \_ WaveFormatEx**           |
| **Estructura de formato** | **FORMA DE ONDAATEX**                   | **FORMA DE ONDAATEX**                   |



 

El miembro **wFormatTag** de la estructura **WAVEATEX** para el audio LPCM es actualmente **WAVE FORMAT \_ \_ UNKNOWN,** pero esto podría cambiar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
