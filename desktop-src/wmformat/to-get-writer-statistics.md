---
title: Para obtener estadísticas del escritor
description: Para obtener estadísticas del escritor
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Formato de sistemas avanzados (ASF), estadísticas de escritor
- ASF (formato de sistemas avanzados), estadísticas de escritor
- estadísticas del escritor, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cedd96f1e94b8d3c9499fe08e3eeebb2100e866b141b756483cfb07bb7cb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083970"
---
# <a name="to-get-writer-statistics"></a>Para obtener estadísticas del escritor

El escritor puede proporcionar información estadística sobre las operaciones de escritura. Hay dos métodos para recopilar estadísticas de escritor: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) e [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex). La información recuperada por **GetStatisticsEx** es más específica que la información recuperada por **GetStatistics**.

Ambos métodos rellenan estructuras con información estadística. **GetStatistics** usa la [**estructura WM WRITER \_ \_ STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) y **GetStatisticsEx** usa la [**estructura WM WRITER \_ \_ STATISTICS \_ EX.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) **GetStatisticsEx** no duplica los datos obtenidos por **GetStatistics.** Para obtener la información más completa, debe llamar a ambos métodos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriterAdvanced (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**IWMWriterAdvanced3 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




