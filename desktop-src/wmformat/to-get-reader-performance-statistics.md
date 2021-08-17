---
title: Para obtener estadísticas de rendimiento del lector
description: Para obtener estadísticas de rendimiento del lector
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Formato de sistemas avanzados (ASF), estadísticas de rendimiento del lector
- ASF (formato de sistemas avanzados), estadísticas de rendimiento del lector
- Formato de sistemas avanzados (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Formato de sistemas avanzados (ASF), estadísticas de rendimiento
- ASF (formato de sistemas avanzados), estadísticas de rendimiento
- lectores asincrónicos, estadísticas de rendimiento
- rendimiento, estadísticas del lector
- rendimiento, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2397e575d67a699c4f211d872b53632e728fc2240b396d7475c8bb6b243fe445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084275"
---
# <a name="to-get-reader-performance-statistics"></a>Para obtener estadísticas de rendimiento del lector

Al leer archivos localmente con el lector asincrónico, no es necesario comprobar el rendimiento de las operaciones de lectura. Sin embargo, si la aplicación está leyendo desde un origen de streaming, las estadísticas de rendimiento pueden ser muy importantes. La aplicación puede responder a los cambios en el rendimiento de la reproducción para garantizar la mejor experiencia posible para el usuario final.

La información de rendimiento que puede recuperar del lector incluye las estadísticas siguientes:

-   Ancho de banda actual de la conexión.
-   Número de paquetes recibidos del servidor.
-   Número de paquetes perdidos que se recuperaron.
-   Número de paquetes perdidos que no se recuperaron.
-   Porcentaje del número total de paquetes enviados que se han recibido.

Para obtener estadísticas de rendimiento del lector, realice los pasos siguientes.

1.  Antes de iniciar la reproducción, cree una [**estructura \_ WM READER \_ STATISTICS.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) Debe establecer el **miembro cbSize** en sizeof(WM \_ READER \_ STATISTICS).
2.  Obtenga un puntero a [**la interfaz IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) del objeto reader llamando a **IWMReader::QueryInterface**.
3.  Durante la reproducción, realice llamadas a [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) con frecuencia para supervisar el rendimiento. Pase la **estructura \_ WM READER \_ STATISTICS** con cada llamada y examine los miembros adecuados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




