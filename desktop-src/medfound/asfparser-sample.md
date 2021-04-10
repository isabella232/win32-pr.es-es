---
description: Ejemplo de ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Ejemplo de ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275150"
---
# <a name="asfparser-sample"></a>Ejemplo de ASFParser

Muestra cómo analizar los datos de un archivo de formato de sistema avanzado (ASF) mediante los componentes ASF de bajo nivel en Media Foundation. En el ejemplo se muestran las tareas siguientes:

-   Enumerar las secuencias de audio y vídeo en un archivo ASF.
-   Seleccionar una secuencia de audio o de vídeo para su análisis.
-   Buscar un paquete en el momento deseado de la reproducción.
-   Generar ejemplos comprimidos para la secuencia seleccionada.
-   Descodificar ejemplos de audio y vídeo.

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de Microsoft Media Foundation:

-   [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>Uso

1.  Para abrir un archivo ASF, haga clic en el botón **Abrir archivo multimedia...** .
2.  Seleccione un archivo ASF y haga clic en **abrir**. En el panel de **información** se muestra información sobre el archivo.
3.  En **configuración del analizador**, seleccione la secuencia que se va a analizar.
4.  Para generar ejemplos en orden inverso, seleccione **inverso**.
5.  Para especificar el punto de inicio, arrastre el control deslizante hasta la ubicación deseada.
6.  Para comenzar el análisis, haga clic en el botón **generar ejemplos** . En el panel de **información** se muestra información sobre los ejemplos.
7.  Para probar los ejemplos de la secuencia de audio, haga clic en el botón **probar audio** .
8.  Para probar los ejemplos de la secuencia de vídeo, haga clic en el botón **Mostrar mapa de bits** .

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Tutorial: lectura de un archivo ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Componentes de WMContainer ASF](wmcontainer-asf-components.md)
</dt> </dl>

 

 



