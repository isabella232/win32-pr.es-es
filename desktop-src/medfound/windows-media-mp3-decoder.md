---
description: El Windows multimedia MP3 descodifica los archivos de audio que se han codificado en los siguientes formatos.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Windows Descodificador MP3 multimedia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58788a00ddaa43686c3cb4be4a52292edb3fe6c6f81fabbc5b4f3e75c47f0f24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737004"
---
# <a name="windows-media-mp3-decoder"></a>Windows Descodificador mp3 multimedia

El Windows multimedia MP3 descodifica los archivos de audio que se han codificado en los siguientes formatos.

-   ISO/IEC 11172-3 (MPEG-1 Audio) Capa 3
-   ISO/IEC 13818-3 (MPEG-2 Audio) Capa 3, extensión de frecuencia de muestreo baja

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador mp3 Windows media se representa mediante la constante **CLSID \_ CMP3DecMediaObject**. Puede crear una instancia del descodificador MP3 llamando a **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objeto descodificador MP3 expone la interfaz **IMediaObject** para que el objeto se pueda usar como un objeto multimedia DirectX (DMO) y expone la interfaz **DETRANSFORMTRANSFORM** para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un descodificador mp3 de Windows Media se comporta como un DMO o un MFT en función de las interfaces que se obtengan y la versión de Windows se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador mp3 Windows media se comporta como un DMO o MFT.



| Sistema operativo | Comportamiento del descodificador                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un Windows multimedia MP3 siempre se comporta como un DMO.                                                                                                                                           |
| Windows Vista    | De forma predeterminada, un Windows multimedia MP3 se comporta como un DMO. Si obtiene una interfaz **IMFTransform** o **una interfaz IPropertyStore** en un descodificador mp3 Windows Media, se comporta como MFT. |
| Windows 7        | De forma predeterminada, un Windows multimedia MP3 se comporta como un DMO. Si obtiene una interfaz **IMFTransform** en un descodificador MP3 Windows Media, se comporta como un MFT.                                    |



 

## <a name="input-formats"></a>Formatos de entrada

En la tabla siguiente se muestra la etiqueta de formato de audio que representa el tipo de entrada admitido por Windows descodificador MP3 multimedia.



| Constante de etiqueta de formato      | Valor de etiqueta de formato | Formato de audio     |
|--------------------------|------------------|------------------|
| FORMATO \_ WAVE \_ MPEGLAYER3 | 0x55             | Capa 3 de ISO MPEG |



 

## <a name="output-formats"></a>Formatos de salida

En la tabla siguiente se muestran las etiquetas de formato de audio que representan los tipos de salida admitidos por Windows descodificador MP3 multimedia.



| Constante de etiqueta de formato       | Valor de etiqueta de formato | Formato de audio                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| WAVE \_ FORMAT \_ PCM         | 0x0001           | Formato PCM (cuando se usa como DMO o MFT)                                   |
| FORMATO WAVE \_ \_ IEEE \_ FLOAT | 0x0003           | Punto flotante IEEE (cuando se usa como MFT)                                   |
| FORMATO \_ WAVE \_ EXTENSIBLE  | 0xFFFE           | Formato PCM/IEEE en **la estructura DESATEXTENSIBLE** (cuando se usa como MFT) |



 

El Windows multimedia MP3 admite y enumera los siguientes tipos de medios de salida.

-   Tipo de salida que tiene la misma frecuencia de muestreo y número de canales que el tipo de entrada.
-   Salida mono para entrada estéreo.
-   Tipos de salida con profundidades de bits de 8 y 16.
-   Salida de punto flotante, si el descodificador se comporta como MFT.

El Windows multimedia MP3 admite, pero no enumera, los siguientes tipos de medios de salida.

-   Tipo de salida que tiene la mitad de la frecuencia de muestreo del tipo de entrada.
-   Tipo de salida que tiene una cuarta parte de la frecuencia de muestreo del tipo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Implementación de códecs](codecimplementation.md)
</dt> </dl>

 

 




