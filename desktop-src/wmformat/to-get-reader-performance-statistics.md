---
title: Para obtener las estadísticas de rendimiento del lector
description: Para obtener las estadísticas de rendimiento del lector
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Advanced Systems Format (ASF), estadísticas de rendimiento de lector
- ASF (formato de sistemas avanzados), estadísticas de rendimiento de lector
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), estadísticas de rendimiento
- ASF (formato de sistemas avanzados), estadísticas de rendimiento
- lectores asincrónicos, estadísticas de rendimiento
- rendimiento, estadísticas de lector
- rendimiento, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904402"
---
# <a name="to-get-reader-performance-statistics"></a>Para obtener las estadísticas de rendimiento del lector

Al leer archivos localmente con el lector asincrónico, no es necesario comprobar el rendimiento de las operaciones de lectura. Sin embargo, si la aplicación lee desde una fuente de streaming, las estadísticas de rendimiento pueden ser muy importantes. La aplicación puede responder a los cambios en el rendimiento de la reproducción para garantizar la mejor experiencia posible del usuario final.

La información de rendimiento que puede recuperar del lector incluye las estadísticas siguientes:

-   Ancho de banda actual de la conexión.
-   El número de paquetes recibidos del servidor.
-   El número de paquetes perdidos que se han recuperado.
-   El número de paquetes perdidos que no se recuperaron.
-   El porcentaje del número total de paquetes enviados que se han recibido.

Para obtener las estadísticas de rendimiento del lector, realice los pasos siguientes.

1.  Antes de iniciar la reproducción, cree una estructura de [**\_ \_ estadísticas del lector de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) . Debe establecer el miembro **cbSize** en sizeof ( \_ estadísticas del lector de WM \_ ).
2.  Obtenga un puntero a la interfaz [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) del objeto lector llamando a **IWMReader:: QueryInterface**.
3.  Durante la reproducción, realice llamadas a [**IWMReaderAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) con frecuencia para supervisar el rendimiento. Pase la estructura de las **\_ \_ estadísticas del lector de WM** con cada llamada y examine los miembros adecuados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




