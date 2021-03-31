---
title: Para buscar números de secuencia y números de salida
description: Para buscar números de secuencia y números de salida
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Advanced Systems Format (ASF), números de secuencia
- ASF (formato de sistemas avanzados), crear números
- Advanced Systems Format (ASF), buscar números de salida
- ASF (formato de sistemas avanzados), buscar números de salida
- lectores sincrónicos, números de secuencia
- lectores sincrónicos, buscar números de salida
- flujos, buscar números
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788739"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>Para buscar números de secuencia y números de salida

El lector sincrónico admite el cambio más simplificado entre los números de flujo y de salida para la reproducción que el lector asincrónico. Por lo tanto, es más importante poder encontrar qué números de secuencia son equivalentes a los números de salida, o viceversa.

Para buscar el número de salida que corresponde a un número de secuencia, llame a [**IWMSyncReader:: GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).

Para buscar el número de secuencia que corresponde a un número de salida, llame a [ **IWMSyncReader:: GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Entradas, secuencias y salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




