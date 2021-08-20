---
description: Descodificador Configuración para Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Descodificador Configuración para Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc373f2ea58bc169748ff42841650cf979822014e579a78459e47da5c694814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953164"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a>Descodificador Configuración para Windows Media Center Edition

Windows XP Media Center Edition 2005 y versiones posteriores usa la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para configurar el filtro de descodificador de audio para televisión y reproducción de DVD. Se admiten las siguientes propiedades.



| GUID de propiedad                   | Descripción                                      |
|---------------------------------|--------------------------------------------------|
| FORMATO DE SALIDA DE AUDIO CODECAPI \_ \_ \_ | Configura el formato de salida de audio. Vea la sección Comentarios. |



 

## <a name="remarks"></a>Comentarios

El valor de la propiedad CODECAPI AUDIO OUTPUT FORMAT es una representación de cadena de \_ \_ un \_ GUID, almacenado como un valor **BSTR.** Se definen los GUID siguientes.



| GUID                                                        | Descripción                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CÓDECAPI \_ AUDIO OUTPUT FORMAT \_ \_ \_ PCM STEREO \_ \_ MATRIXENCODED | El filtro de audio de software debe realizar la descodificación de software y generar una secuencia de audio estéreo, con la matriz de audio multicanal codificada en los dos canales.                                                   |
| CODECAPI \_ AUDIO \_ OUTPUT \_ FORMAT \_ PCM \_ STEREO                | El filtro de audio de software debe realizar la decodificación de software y generar una secuencia de audio estéreo.                                                                                                                   |
| CODECAPI \_ AUDIO \_ OUTPUT \_ FORMAT \_ SPDIF \_ PCM                 | El filtro de audio de software debe realizar la codificación de audio de software, aunque la salida física del equipo pueda ser una interfaz digital, como S/PDIF.                                                      |
| CODECAPI \_ AUDIO \_ OUTPUT \_ FORMAT \_ SPDIF \_ BITSTREAM           | El filtro de audio de software no debe realizar la codificación de audio de software, pero debe pasar la secuencia de bits de audio digital sin procesar para el procesamiento externo por un dispositivo conectado con un vínculo de audio digital, como S/PDIF. |
| CASCOS \_ \_ PCM CON \_ FORMATO DE SALIDA DE AUDIO \_ \_ CODECAPI            | El filtro de audio de software debe realizar la decodificación de audio de software y debe aplicar el procesamiento propietario para optimizar los cascos. La compatibilidad con esta configuración es opcional.                                     |



 

> [!Note]  
> La **interfaz ICodecAPI** almacena las propiedades de códec como pares clave-valor, donde la clave es un GUID y el valor es **un tipo VARIANT.**

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de codificadores y descodificadores](encoder-and-decoder-development.md)
</dt> </dl>

 

 



