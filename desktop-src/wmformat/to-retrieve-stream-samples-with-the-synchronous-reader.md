---
title: Para recuperar ejemplos de secuencias con el lector sincrónico
description: Para recuperar ejemplos de secuencias con el lector sincrónico
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- Advanced Systems Format (ASF), recuperar ejemplos de secuencias
- ASF (formato de sistemas avanzados), recuperar ejemplos de secuencias
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, recuperar ejemplos de secuencias
- flujos, recuperar ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149080"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a>Para recuperar ejemplos de secuencias con el lector sincrónico

Al igual que el lector asincrónico, el lector sincrónico puede recuperar muestras por número de secuencia. A diferencia del lector asincrónico, el lector sincrónico puede proporcionar ejemplos de secuencias comprimidos o sin comprimir.

Para recibir ejemplos de secuencias, realice los pasos siguientes.

1.  En cualquier momento antes o durante la reproducción, llame a [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) pasando el número de flujo deseado.
2.  Recupere ejemplos con llamadas continuas a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).

Puede comprobar si se ha seleccionado una secuencia para la entrega de ejemplo llamando a [**IWMSyncReader:: GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




