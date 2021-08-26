---
description: Compatibilidad con MPEG-2 en DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Compatibilidad con MPEG-2 en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9feaa24ea36b6f5e00e0f6ecd5db49ce37181f9d6d7348b3cfa27e64f7f2d84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075805"
---
# <a name="mpeg-2-support-in-directshow"></a>Compatibilidad con MPEG-2 en DirectShow

En esta sección se describen los componentes que puede usar para reproducir contenido MPEG-2 en DirectShow.

> [!Note]  
> Aunque el vídeo de DVD se basa en MPEG-2, en esta sección no se describe la reproducción o navegación de DVD. Para obtener información sobre DVD en DirectShow, vea [Aplicaciones de DVD](dvd-applications.md).

 

Los datos MPEG-2 pueden provienen de un archivo local o de un origen en directo, como una difusión de red o un dispositivo D-VHS. La reproducción de archivos se denomina *modo* de extracción porque el filtro del analizador extrae datos del archivo en el gráfico de filtros. Los orígenes en directo se *denominan modo* de inserción porque el filtro de origen inserta datos en el gráfico.

DirectShow proporciona dos filtros que pueden analizar secuencias del sistema MPEG-2:

-   [Mpeg-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): este filtro admite el modo de inserción para secuencias de programa y secuencias de transporte. En Windows XP y versiones posteriores, también admite el modo de extracción para secuencias de programa.
-   [Divisor MPEG-2:](mpeg-2-splitter.md)este filtro admite el modo de extracción para secuencias de programa en plataformas de nivel inferior. Este filtro está en desuso en Windows XP y versiones posteriores.

Para usar el divisor MPEG-2 demux o MPEG-2 DirectShow, debe tener descodificadores de audio y vídeo MPEG-2 compatibles con MPEG-2 que acepten secuencias elementales en paquetes (PES).

Esta sección contiene los siguientes temas:

-   [Introducción a los sistemas MPEG-2](overview-of-mpeg-2-systems.md)
-   [Uso del demultiplexor MPEG-2](using-the-mpeg-2-demultiplexer.md)
-   [Uso del divisor MPEG-2](using-the-mpeg-2-splitter.md)
-   [Propiedades de ejemplo MPEG](mpeg-sample-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de filtro del analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 



