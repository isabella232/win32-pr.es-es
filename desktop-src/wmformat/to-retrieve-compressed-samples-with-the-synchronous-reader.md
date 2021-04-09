---
title: Para recuperar muestras comprimidas con el lector sincrónico
description: Para recuperar muestras comprimidas con el lector sincrónico
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Advanced Systems Format (ASF), recuperar muestras comprimidas
- ASF (formato de sistemas avanzados), recuperar ejemplos comprimidos
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- Advanced Systems Format (ASF), ejemplos comprimidos
- ASF (formato de sistemas avanzados), ejemplos comprimidos
- lectores sincrónicos, recuperar ejemplos comprimidos
- lectores sincrónicos, ejemplos comprimidos
- ejemplos comprimidos, recuperar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149082"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>Para recuperar muestras comprimidas con el lector sincrónico

Al igual que el lector asincrónico, el lector sincrónico también puede recuperar ejemplos comprimidos. Los ejemplos comprimidos deben usarse al copiar transmisiones de un archivo a otro.

El SDK de Windows Media Format no proporciona ningún método para descodificar los datos una vez extraídos de un archivo ASF. Si recibe ejemplos comprimidos y posteriormente desea descomprimirlos, tendrá que proporcionar su propio código para hacerlo. Una manera de solucionar esta limitación es escribir los ejemplos comprimidos en un nuevo archivo ASF y, a continuación, volver a leerlos en ejemplos normales y sin comprimir.

Para recibir muestras comprimidas con el lector sincrónico, llame a [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) antes o durante la reproducción. Pase True para *fCompressed*.

> [!Note]  
> Los flujos de imagen no son válidos para la entrega de secuencias comprimidas. Si copia una secuencia de imágenes de un archivo a otro, no funcionará en el nuevo archivo. Para copiar un flujo de imagen de archivo a archivo, recupere los ejemplos de flujo de imagen por número de salida e inclúyalo en el nuevo archivo como si se incluira una nueva secuencia de imágenes.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




