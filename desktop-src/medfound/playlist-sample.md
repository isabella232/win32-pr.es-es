---
description: Ejemplo de lista de reproducción
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Ejemplo de lista de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715509"
---
# <a name="playlist-sample"></a>Ejemplo de lista de reproducción

Muestra cómo utilizar Microsoft Media Foundation para reproducir una secuencia de archivos de audio en una lista de reproducción. En el ejemplo se usa el [origen del secuenciador](sequencer-source.md) para crear y administrar la lista de reproducción.

> [!Note]  
> Este ejemplo ya no se incluye en el SDK de.

 

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de Media Foundation:

-   [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>Uso

El ejemplo de lista de reproducción crea una aplicación de Windows.

-   Para crear una nueva lista de reproducción, seleccione **Agregar a lista de reproducción** en el menú **archivo** . En el cuadro de diálogo **Abrir archivo** , seleccione uno o más archivos de audio. Los archivos se agregan a la lista de reproducción.
-   Para reproducir la secuencia, haga clic en **reproducir**.
-   Para pausar el segmento actual, haga clic en **pausar**.
-   Para detener el segmento actual, haga clic en **detener**.
-   Para ir a un archivo, haga doble clic en el elemento en la lista de reproducción.
-   Para eliminar un archivo de la lista de reproducción, seleccione el elemento en la lista de reproducción. A continuación, seleccione **quitar de la lista de reproducción** en el menú **archivo** .

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location                                                     | Ruta de acceso/URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [Windows SDK](https://www.microsoft.com/download/details.aspx?id=8279) | *Raíz* \\ del SDK Ejemplo \\ de \\ lista de reproducción multimedia mediafoundation \\ |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de BasicPlayback](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 
