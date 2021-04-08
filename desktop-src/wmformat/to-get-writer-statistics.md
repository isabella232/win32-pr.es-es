---
title: Para obtener estadísticas del escritor
description: Para obtener estadísticas del escritor
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Advanced Systems Format (ASF), estadísticas del escritor
- ASF (formato de sistemas avanzados), estadísticas del escritor
- Estadísticas del escritor, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103995024"
---
# <a name="to-get-writer-statistics"></a>Para obtener estadísticas del escritor

El escritor puede proporcionar información estadística acerca de las operaciones de escritura. Hay dos métodos para recopilar estadísticas del escritor: [**IWMWriterAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) y [**IWMWriterAdvanced3:: GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). La información recuperada por **GetStatisticsEx** es más específica que la información recuperada por **GetStatistics**.

Ambos métodos rellenan las estructuras con información estadística. **GetStatistics** usa la estructura de [**\_ \_ estadísticas del escritor de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) y **GetStatisticsEx** usa la estructura de estadísticas del [**escritor de WM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) . **GetStatisticsEx** no duplica los datos obtenidos por **GetStatistics**. Para obtener la información más completa, debe llamar a ambos métodos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interfaz IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




