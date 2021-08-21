---
title: Para buscar por tiempo mediante el lector sincrónico
description: Para buscar por tiempo mediante el lector sincrónico
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Formato de sistemas avanzados (ASF), búsqueda por hora
- ASF (formato de sistemas avanzados), búsqueda por hora
- Formato de sistemas avanzados (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, búsqueda por hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74fb0cb4f73e70821347b82a9e5a2544eb9759e733fb164077b2fc007163db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432638"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>Para buscar por tiempo mediante el lector sincrónico

Para buscar datos mediante el lector sincrónico, especifique un intervalo para la reproducción. Un intervalo se define mediante un tiempo de presentación inicial y una duración, ambos en unidades de 100 nanosegundos.

Para buscar datos en un archivo ASF por tiempo de presentación mediante el lector sincrónico, realice los pasos siguientes.

1.  Especifique una hora de inicio y una duración para la entrega de ejemplo mediante una [**llamada a IWMSyncReader::SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange). Este método no requiere que especifique un número de secuencia porque los tiempos de presentación de cada secuencia ya deben estar sincronizados.
2.  Comience a recuperar ejemplos con llamadas a [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Continúe como lo haría normalmente con el lector sincrónico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lectura de archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




