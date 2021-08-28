---
description: Tipos de medios de demultiplexador MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipos de medios de demultiplexador MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dfba52378813b8b96920a44c593e9c7d4b45a0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476281"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>Tipos de medios de demultiplexador MPEG-2

El [filtro Demultiplexer MPEG-2](mpeg-2-demultiplexer.md) reconoce los siguientes tipos de medios.

### <a name="input-types"></a>Tipos de entrada

El tipo principal es siempre **MEDIATYPE \_ Stream.** El subtipo puede ser cualquiera de los siguientes.



| GUID                                             | Descripción                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TRANSPORTE DE \_ \_ BDA \_ MPEG2 DEL SUBTIPO KSDATAFORMAT \_** | Flujo de transporte desde un filtro de dispositivo de arquitectura de controlador de difusión (BDA). El demultiplexador MPEG-2 trata este subtipo de forma idéntica a **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**.                                |
| **PROGRAMA \_ MPEG2 DE MEDIASUBTYPE \_**                 | Secuencia de programa                                                                                                                                                                                            |
| **TRANSPORTE DE MEDIASUBTYPE \_ MPEG2 \_**               | Secuencia de transporte (TS), con paquetes de 188 bytes                                                                                                                                                              |
| **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE**       | Flujo de transporte con paquetes "strided". Este subtipo indica que los paquetes TS se pueden agregar con bytes adicionales. Para obtener más información, [**vea MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md). |



 

Para los paquetes de transporte strided **(MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE),** cada ejemplo multimedia debe contener un número entero de paquetes de transporte, como se describe en [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md). Para todos los demás tipos de entrada, no hay ninguna restricción en los límites de ejemplo; los paquetes individuales pueden abarcar límites de ejemplo.

### <a name="output-types"></a>Tipos de salida

El demultiplexador MPEG-2 no valida los tipos de salida; El filtro de nivel inferior es responsable de analizar los datos que recibe del demultiplexor. Sin embargo, los siguientes tipos se aceptan normalmente mediante filtros de nivel inferior como salida del demultiplexor.

### <a name="mpeg-2-sections"></a>Secciones mpeg-2




| | | Tipo principal | <strong>MEDIATYPE_MPEG2_SECTIONS</strong> | | Subtipo | Cualquiera de las siguientes opciones:<br /><ul><li><strong>MEDIASUBTYPE_ATSC_SI:</strong>información del servicio ATSC.</li><li><strong>MEDIASUBTYPE_DVB_SI:</strong>información del servicio DE TRAS.</li><li><strong>MEDIASUBTYPE_ISDB_SI:</strong>Información del servicio de difusión digital de servicios integrados (ISDB).</li><li><strong>MEDIASUBTYPE_MPEG2DATA:</strong>datos de la sección MPEG-2.</li></ul> | | Formato de tipo | Ninguno | 




 

### <a name="mpeg-2-video"></a>Vídeo MPEG-2



| Etiqueta | Valor |
|------------------|------------------------------------------|
| Tipo principal       | **Vídeo \_ DE MEDIATYPE**                     |
| Subtype          | **VÍDEO DE MEDIASUBTYPE \_ MPEG2 \_**           |
| Tipo de formato      | **FORMAT \_ MPEG2Video**                   |
| Estructura de formato | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>MPEG-2 Audio



| Etiqueta | Valor |
|------------------|--------------------------------------|
| Tipo principal       | **MEDIATYPE \_ Audio**                 |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**       |
| Tipo de formato      | **FORMAT \_ WaveFormatEx**             |
| Estructura de formato | [**FORMA DE ONDAATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
