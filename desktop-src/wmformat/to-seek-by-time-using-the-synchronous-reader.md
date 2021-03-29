---
title: Para buscar por tiempo mediante el lector sincrónico
description: Para buscar por tiempo mediante el lector sincrónico
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- Advanced Systems Format (ASF), búsqueda por tiempo
- ASF (formato de sistemas avanzados), búsqueda por hora
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, búsquedas por tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788811"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>Para buscar por tiempo mediante el lector sincrónico

Para buscar datos mediante el lector sincrónico, especifique un intervalo para la reproducción. Un intervalo se define mediante un tiempo de presentación inicial y una duración, ambos en unidades de 100-nanosegundos.

Para buscar datos en un archivo ASF por tiempo de presentación mediante el lector sincrónico, realice los pasos siguientes.

1.  Especifique una hora de inicio y una duración para la entrega de ejemplo llamando a [**IWMSyncReader:: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange). Este método no requiere que se especifique un número de secuencia porque los tiempos de presentación de cada flujo ya deben estar sincronizados.
2.  Comience a recuperar ejemplos con llamadas a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Continúe como lo haría normalmente con el lector sincrónico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




