---
description: Ejemplo de ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Ejemplo de ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361183"
---
# <a name="asfparser-sample"></a>Ejemplo de ASFParser

Muestra cómo analizar datos de un archivo de formato de sistemas avanzados (ASF) mediante los componentes de ASF de bajo nivel en Media Foundation. En el ejemplo se muestran las siguientes tareas:

-   Enumerar las secuencias de audio y vídeo en un archivo ASF.
-   Seleccionar una secuencia de audio o vídeo para analizarla.
-   Buscar un paquete en el momento de reproducción deseado.
-   Generación de muestras comprimidas para la secuencia seleccionada.
-   Decoding audio and video samples (Decoding audio and video samples).

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las Microsoft Media Foundation siguientes:

-   [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>Uso

1.  Para abrir un archivo ASF, haga clic en **el botón Abrir archivo multimedia....**
2.  Seleccione un archivo ASF y haga clic **en Abrir.** La información sobre el archivo se muestra en el **panel** Información.
3.  En **Configuración del analizador,** seleccione una secuencia para analizar.
4.  Para generar ejemplos a la inversa, seleccione **Invertir.**
5.  Para especificar el punto de inicio, arrastre el control deslizante a la ubicación deseada.
6.  Para comenzar el análisis, haga clic en **el botón Generar** ejemplos. La información sobre los ejemplos se muestra en el **panel** Información.
7.  Para probar los ejemplos de la secuencia de audio, haga clic en el **botón Probar** audio.
8.  Para probar los ejemplos de la secuencia de vídeo, haga clic en el **botón Mostrar mapa de** bits.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de github Windows ejemplos clásicos](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Tutorial: Lectura de un archivo ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Componentes de ASF de WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



