---
title: Para el uso de telecine inverso
description: Para el uso de telecine inverso
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Media Format SDK, Telecine inverso
- SDK de Windows Media Format, telecine
- Advanced Systems Format (ASF), Telecine inverso
- ASF (formato de sistemas avanzados), Telecine inverso
- Advanced Systems Format (ASF), telecine
- ASF (formato de sistemas avanzados), telecine
- Telecine inverso
- Telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105695572"
---
# <a name="to-use-inverse-telecine"></a>Para el uso de telecine inverso

Telecine es el proceso de convertir película, que tiene 24 fotogramas por segundo, en vídeo, que tiene 60 campos (medio fotogramas) por segundo. Este proceso coloca las imágenes de cada fotograma de la película en varios campos de vídeo.

Al codificar digitalmente un vídeo que se creó a partir de una película mediante telecine, el proceso de compresión puede producir artefactos de movimiento y otras disminuciones de calidad. Para evitar que afecte a la calidad de la salida digital, el códec de Windows Media Video 9 admite telecine inversa. Cuando se usa Telecine inverso, el códec reconstruye los fotogramas de la película 24 originales por segundo del vídeo de entrada antes de codificar el contenido.

Para usar telecine inversa, debe:

-   Use un perfil con una secuencia de vídeo establecida en 24 fotogramas por segundo.
-   Conozca la configuración de campo del vídeo de entrada.

Para usar telecine inversa para una entrada al escritor, realice los pasos siguientes.

1.  Configure el escritor como de costumbre. Para obtener más información, consulte [Writing ASF files](writing-asf-files.md).
2.  Antes de empezar a escribir ejemplos, obtenga un puntero a la interfaz [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) llamando a **IWMWriter:: QueryInterface**.
3.  Identifique la secuencia que se va a reconstruir mediante una llamada a [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para el número de entrada deseado. Pase g \_ wszDeinterlaceMode como la configuración y WM \_ DM \_ desentrelazado \_ INVERSETELECINE como valor.
4.  Vuelva a llamar a **SetInputSetting** para establecer g \_ wszInitialPatternForInverseTelecine.
5.  Escriba el archivo como de costumbre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> <dt>

[**Interfaz IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interfaz IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




