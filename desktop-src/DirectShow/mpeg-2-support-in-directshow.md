---
description: Compatibilidad con MPEG-2 en DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Compatibilidad con MPEG-2 en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537798"
---
# <a name="mpeg-2-support-in-directshow"></a>Compatibilidad con MPEG-2 en DirectShow

En esta sección se describen los componentes que puede usar para reproducir contenido MPEG-2 en DirectShow.

> [!Note]  
> Aunque DVD video se basa en MPEG-2, esta sección no describe la reproducción ni la navegación por DVD. Para obtener información acerca del DVD en DirectShow, consulte [aplicaciones de DVD](dvd-applications.md).

 

Los datos MPEG-2 pueden provienen de un archivo local o de un origen en directo, como una difusión de red o un dispositivo D-VHS. La reproducción de archivos se denomina *modo de extracción* porque el filtro del analizador extrae los datos del archivo en el gráfico de filtro. Los orígenes en directo se denominan el *modo de extracción* porque el filtro de origen envía datos al gráfico.

DirectShow proporciona dos filtros que pueden analizar secuencias del sistema MPEG-2:

-   [Demultiplexador MPEG-2](mpeg-2-demultiplexer.md) ("Demux"): este filtro admite el modo de extracción para flujos de programa y secuencias de transporte. En Windows XP y versiones posteriores, también admite el modo de extracción para las secuencias de programa.
-   [Separador MPEG-2](mpeg-2-splitter.md): este filtro admite el modo de extracción para las secuencias de programa en plataformas de nivel inferior. Este filtro está en desuso en Windows XP y versiones posteriores.

Para usar el separador MPEG-2 Demux o MPEG-2, debe tener descodificadores de audio y vídeo de MPEG-2 compatibles con DirectShow que acepten secuencias elementales (PES).

Esta sección contiene los siguientes temas:

-   [Información general de los sistemas MPEG-2](overview-of-mpeg-2-systems.md)
-   [Usar el demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
-   [Usar el divisor MPEG-2](using-the-mpeg-2-splitter.md)
-   [Propiedades de ejemplo MPEG](mpeg-sample-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de filtro de analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 



