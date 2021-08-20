---
title: Para el uso de telecine inverso
description: Para el uso de telecine inverso
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows SDK de formato multimedia, televisa inversa
- Windows SDK de formato multimedia, televisa
- Formato de sistemas avanzados (ASF), televisa inversa
- ASF (formato de sistemas avanzados), televisa inversa
- Formato de sistemas avanzados (ASF), televisa
- ASF (formato de sistemas avanzados), televisa
- tele telefónica inversa
- Telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7885caffea83460d73b1eca26dbfd94eb50d99ac4aa8589113875ffc4358c029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585325"
---
# <a name="to-use-inverse-telecine"></a>Para el uso de telecine inverso

Telecinco es el proceso de convertir película, que tiene 24 fotogramas por segundo, en vídeo, que tiene 60 campos (medio fotogramas) por segundo. Este proceso coloca imágenes de cada fotograma de película en varios campos de vídeo.

Al codificar digitalmente un vídeo que se creó a partir de una película mediante televisa, el proceso de compresión puede provocar artefactos de movimiento y otras degradaciones de calidad. Para evitar que afecte a la calidad de la salida digital, el códec Windows Media Video 9 admite televersión inversa. Cuando se usa la tele tele telefónica inversa, el códec reconstruye los 24 fotogramas originales por segundo del vídeo de entrada antes de codificar el contenido.

Para usar televisa inversa, debe:

-   Use un perfil con una secuencia de vídeo establecida en 24 fotogramas por segundo.
-   Conozca la configuración de campo del vídeo de entrada.

Para usar televisa inversa para una entrada al escritor, realice los pasos siguientes.

1.  Configure el escritor como de costumbre. Para obtener más información, vea [Escribir archivos ASF.](writing-asf-files.md)
2.  Antes de empezar a escribir ejemplos, obtenga un puntero a la [**interfaz IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) mediante una llamada a **IWMWriter::QueryInterface**.
3.  Identifique la secuencia que se va a reconstruir llamando a [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para el número de entrada deseado. Pase g \_ wszDeinterlaceMode como valor y WM \_ DM \_ DEINTERLACE \_ INVERSETELEDIV como valor.
4.  Llame de nuevo a **SetInputSetting** para establecer g \_ wszInitialPatternForInverseTeleversión.
5.  Escriba el archivo como de costumbre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Temas avanzados**](advanced-topics.md)
</dt> <dt>

[**IWMWriter (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**IWMWriterAdvanced2 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




