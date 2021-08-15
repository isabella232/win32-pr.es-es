---
title: Para buscar números de flujo y números de salida
description: Para buscar números de flujo y números de salida
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Formato de sistemas avanzados (ASF), números de secuencia
- ASF (formato de sistemas avanzados), creación de números
- Formato de sistemas avanzados (ASF), buscar números de salida
- ASF (formato de sistemas avanzados), buscar números de salida
- lectores sincrónicos, números de secuencia
- lectores sincrónicos, buscar números de salida
- streams,finding numbers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4349bc98214d61a1529fe4a64dd142a9695d909f9e2a650162a8e4f8ac618177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699593"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a>Para buscar números de flujo y números de salida

El lector sincrónico admite un cambio más simplificado entre los números de secuencia y salida para la reproducción que el lector asincrónico. Por lo tanto, es más importante poder encontrar qué números de flujo equivalen a los números de salida o al revés.

Para buscar el número de salida que corresponde a un número de secuencia, llame a [**IWMSyncReader::GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).

Para buscar el número de secuencia que corresponde a un número de salida, llame a [ **IWMSyncReader::GetStreamNumberForOutput.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lectura de archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




