---
description: Configuración del descodificador para Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Configuración del descodificador para Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105660007"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a>Configuración del descodificador para Windows Media Center Edition

Windows XP Media Center Edition 2005 y versiones posteriores usan la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para configurar el filtro de descodificador de audio para la reproducción de televisión y DVD. Se admiten las siguientes propiedades.



| GUID de propiedad                   | Descripción                                      |
|---------------------------------|--------------------------------------------------|
| \_formato de \_ salida de audio CODECAPI \_ | Configura el formato de salida de audio. Vea la sección Comentarios. |



 

## <a name="remarks"></a>Observaciones

El valor de la \_ propiedad CODECAPI audio \_ Output \_ Format es una representación de cadena de un GUID, que se almacena como un valor **BSTR** . Se definen los siguientes GUID.



| GUID                                                        | Descripción                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_formato de salida de audio CODECAPI \_ \_ \_ PCM \_ estéreo \_ MATRIXENCODED | El filtro de audio de software debe realizar la descodificación de software y generar una secuencia de audio estéreo con la matriz de audio multicanal codificada en los dos canales.                                                   |
| \_formato de salida de audio CODECAPI \_ \_ \_ PCM \_ Stereo                | El filtro de audio de software debe realizar la descodificación de software y generar una secuencia de audio estéreo.                                                                                                                   |
| \_formato de salida de audio CODECAPI \_ \_ \_ \_ PCM SPDIF                 | El filtro de audio de software debe realizar la descodificación de audio de software, aunque la salida física del equipo puede ser una interfaz digital, como S/PDIF.                                                      |
| \_formato de salida de audio CODECAPI \_ \_ \_ SPDIF \_ fragmentada           | El filtro de audio de software no debe realizar la descodificación de audio de software, pero debe pasar el fragmentada de audio digital sin procesar para el procesamiento externo por un dispositivo conectado a un vínculo de audio digital, como S/PDIF. |
| formato de salida de audio CODECAPI- \_ \_ \_ \_ \_ auriculares PCM            | El filtro de audio de software debe realizar la descodificación de audio de software y debe aplicar el procesamiento de propiedad para optimizar los auriculares. La compatibilidad con esta configuración es opcional.                                     |



 

> [!Note]  
> La interfaz **ICodecAPI** almacena las propiedades de códec como pares clave-valor, donde la clave es un GUID y el valor es un tipo **Variant** .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo del codificador y descodificador](encoder-and-decoder-development.md)
</dt> </dl>

 

 



