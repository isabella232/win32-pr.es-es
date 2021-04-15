---
description: Tipos de medios de demultiplexador MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipos de medios de demultiplexador MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689658"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>Tipos de medios de demultiplexador MPEG-2

El filtro de [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) reconoce los siguientes tipos de medios.

### <a name="input-types"></a>Tipos de entrada

El tipo principal siempre es **el \_ flujo de MEDIATYPE**. El subtipo puede ser cualquiera de los siguientes.



| GUID                                             | Descripción                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Subtipo de KSDATAFORMAT de \_ \_ \_ transporte MPEG2 BDA \_** | Secuencia de transporte de un filtro de dispositivo de la arquitectura de controlador de difusión (BDA). El desmultiplexador MPEG-2 trata este subtipo de manera idéntica a **MEDIASUBTYPE \_ MPEG2 \_ Transport**.                                |
| **\_Programa MPEG2 de MEDIASUBTYPE \_**                 | Secuencia de programa                                                                                                                                                                                            |
| **\_Transporte MPEG2 de MEDIASUBTYPE \_**               | Secuencia de transporte (TS), con paquetes de 188 bytes                                                                                                                                                              |
| **\_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_**       | Secuencia de transporte con paquetes "progresados". Este subtipo indica que los paquetes de TS se pueden rellenar con bytes adicionales. Para obtener más información, [**consulte \_ \_ intervalo de transporte de MPEG2**](mpeg2-transport-stride.md). |



 

En el caso de los paquetes de transporte más progresados (intervalo de transporte de MPEG2 de MEDIASUBTYPE), cada ejemplo de medio debe contener un número entero de paquetes de transporte, tal y como se describe en [**intervalo de \_ transporte \_ de MPEG2**](mpeg2-transport-stride.md).**\_ \_ \_** Para el resto de tipos de entrada, no hay restricciones en los límites de muestra; los paquetes individuales pueden abarcar los límites de ejemplo.

### <a name="output-types"></a>Tipos de salida

El desmultiplexador MPEG-2 no valida los tipos de salida; el filtro de nivel inferior es responsable de analizar los datos que recibe del desmultiplexador. Sin embargo, los filtros inferiores aceptan normalmente los siguientes tipos como resultado del desmultiplexador.

### <a name="mpeg-2-sections"></a>Secciones MPEG-2



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Tipo principal</td>
<td><strong>MEDIATYPE_MPEG2_SECTIONS</strong></td>
</tr>
<tr class="even">
<td>Subtype</td>
<td>Cualquiera de los siguientes:<br/>
<ul>
<li><strong>MEDIASUBTYPE_ATSC_SI</strong>: información del servicio ATSC.</li>
<li><strong>MEDIASUBTYPE_DVB_SI</strong>: información del servicio DVB.</li>
<li><strong>MEDIASUBTYPE_ISDB_SI</strong>: información del servicio de difusión digital de servicios integrados (ISDB).</li>
<li><strong>MEDIASUBTYPE_MPEG2DATA</strong>: datos de la sección MPEG-2.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tipo de formato</td>
<td>None</td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a>Vídeo MPEG-2



|                  |                                          |
|------------------|------------------------------------------|
| Tipo principal       | **Vídeo de MEDIATYPE \_**                     |
| Subtype          | **\_Vídeo MPEG2 de MEDIASUBTYPE \_**           |
| Tipo de formato      | **FORMATO \_ MPEG2Video**                   |
| Estructura de formato | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>Audio MPEG-2



|                  |                                      |
|------------------|--------------------------------------|
| Tipo principal       | **Audio de MEDIATYPE \_**                 |
| Subtype          | **\_Audio MPEG2 de MEDIASUBTYPE \_**       |
| Tipo de formato      | **DAR formato a \_ WaveFormatEx**             |
| Estructura de formato | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
