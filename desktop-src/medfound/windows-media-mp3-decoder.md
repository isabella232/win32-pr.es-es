---
description: El descodificador MP3 de Windows Media descodifica archivos de audio que se han codificado en los siguientes formatos.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Descodificador MP3 de Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700212"
---
# <a name="windows-media-mp3-decoder"></a>Descodificador MP3 de Windows Media

El descodificador MP3 de Windows Media descodifica archivos de audio que se han codificado en los siguientes formatos.

-   ISO/IEC 11172-3 (audio MPEG-1) capa 3
-   ISO/IEC 13818-3 (MPEG-2 audio) de nivel 3, extensión de frecuencia de muestreo bajo

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) para el descodificador MP3 de Windows Media se representa mediante la **constante \_ CMP3DecMediaObject de CLSID**. Puede crear una instancia del descodificador MP3 llamando a **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Un objeto descodificador MP3 expone la interfaz **IMediaObject** para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y expone la interfaz **IMFTransform** para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un descodificador MP3 de Windows Media se comporta como un DMO o una MFT en función de las interfaces que se obtengan y de la versión de Windows que se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador MP3 de Windows Media se comporta como un DMO o MFT.



| Sistema operativo | Comportamiento del descodificador                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Un descodificador MP3 de Windows Media siempre se comporta como DMO.                                                                                                                                           |
| Windows Vista    | De forma predeterminada, un descodificador MP3 de Windows Media se comporta como un DMO. Si obtiene una interfaz **IMFTransform** o una interfaz **IPropertyStore** en un descodificador MP3 de Windows Media, se comporta como una MFT. |
| Windows 7        | De forma predeterminada, un descodificador MP3 de Windows Media se comporta como un DMO. Si obtiene una interfaz **IMFTransform** en un descodificador MP3 de Windows Media, se comporta como una MFT.                                    |



 

## <a name="input-formats"></a>Formatos de entrada

En la tabla siguiente se muestra la etiqueta de formato de audio que representa el tipo de entrada que admite el descodificador MP3 de Windows Media.



| Format (constante de etiqueta)      | Valor de etiqueta de formato | Formato de audio     |
|--------------------------|------------------|------------------|
| Formato de onda \_ \_ MPEGLAYER3 | 0x55             | ISO MPEG nivel 3 |



 

## <a name="output-formats"></a>Formatos de salida

En la tabla siguiente se muestran las etiquetas de formato de audio que representan los tipos de salida admitidos por el descodificador MP3 de Windows Media.



| Format (constante de etiqueta)       | Valor de etiqueta de formato | Formato de audio                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| \_PCM con formato de onda \_         | 0x0001           | Formato PCM (cuando se usa como DMO o MFT)                                   |
| \_formato Wave \_ IEEE \_ float | 0x0003           | Punto flotante IEEE (cuando se usa como MFT)                                   |
| formato de onda \_ \_ extensible  | 0xFFFE           | Formato PCM/IEEE en la estructura **WAVEFORMATEXTENSIBLE** (cuando se usa como MFT) |



 

El descodificador MP3 de Windows Media admite y enumera los siguientes tipos de medios de salida.

-   Un tipo de salida que tiene la misma velocidad de muestreo y número de canales que el tipo de entrada.
-   Salida mono para entrada estéreo.
-   Tipos de salida con profundidades de bits de 8 y 16.
-   Salida de punto flotante, si el descodificador se comporta como MFT.

El descodificador MP3 de Windows Media admite, pero no enumera, los siguientes tipos de medios de salida.

-   Tipo de salida que tiene la mitad de la frecuencia de muestreo del tipo de entrada.
-   Un tipo de salida que tiene un cuarto de la frecuencia de muestreo del tipo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Implementación de códecs](codecimplementation.md)
</dt> </dl>

 

 




