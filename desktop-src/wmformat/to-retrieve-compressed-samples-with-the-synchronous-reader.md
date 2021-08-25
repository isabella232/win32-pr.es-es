---
title: Para recuperar ejemplos comprimidos con el lector sincrónico
description: Para recuperar ejemplos comprimidos con el lector sincrónico
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Formato de sistemas avanzados (ASF), recuperación de muestras comprimidas
- ASF (formato de sistemas avanzados), recuperación de muestras comprimidas
- Formato de sistemas avanzados (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- Formato de sistemas avanzados (ASF), ejemplos comprimidos
- ASF (formato de sistemas avanzados), ejemplos comprimidos
- lectores sincrónicos, recuperación de muestras comprimidas
- lectores sincrónicos, ejemplos comprimidos
- ejemplos comprimidos, recuperación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eeb2e3c7f1f6e00bd3f1c215a3b6783387fd3e19c268afe58862aa4b4d61889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807465"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>Para recuperar ejemplos comprimidos con el lector sincrónico

Al igual que el lector asincrónico, el lector sincrónico también puede recuperar muestras comprimidas. Se deben usar ejemplos comprimidos al copiar secuencias de un archivo a otro.

El SDK Windows Media Format no proporciona ningún método para la decodificación de datos una vez extraídos de un archivo ASF. Si recibe ejemplos comprimidos y posteriormente desea descomprimirlos, tendrá que proporcionar su propio código para hacerlo. Una manera de evitar esta limitación es escribir las muestras comprimidas en un nuevo archivo ASF y, a continuación, volver a leerlas en muestras normales y sin comprimir.

Para recibir muestras comprimidas con el lector sincrónico, llame a [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) antes o durante la reproducción. Pase true para *fCompressed.*

> [!Note]  
> Los flujos de imágenes no son válidos para la entrega de secuencias comprimidas. Si copia una secuencia de imágenes de un archivo a otro, no funcionará en el nuevo archivo. Para copiar un flujo de imagen de un archivo a otro, recupere los ejemplos de secuencia de imágenes por número de salida e incluyéndolos en el nuevo archivo como si incluyese una nueva secuencia de imágenes.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




