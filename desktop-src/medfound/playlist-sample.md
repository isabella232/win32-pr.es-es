---
description: Ejemplo de lista de reproducción
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Ejemplo de lista de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580241"
---
# <a name="playlist-sample"></a>Ejemplo de lista de reproducción

Muestra cómo usar Microsoft Media Foundation reproducir una secuencia de archivos de audio en una lista de reproducción. En el ejemplo se usa [el origen del secuenciador](sequencer-source.md) para crear y administrar la lista de reproducción.

> [!Note]  
> Este ejemplo ya no se incluye en el SDK.

 

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las siguientes Media Foundation interfaces:

-   [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>Uso

El ejemplo de lista de reproducción compila Windows aplicación.

-   Para crear una nueva lista de reproducción, seleccione **Agregar a lista de reproducción** en el **menú** Archivo. En el **cuadro de diálogo Abrir** archivo, seleccione uno o varios archivos de audio. Los archivos se agregan a la lista de reproducción.
-   Para reproducir la secuencia, haga clic en **Reproducir**.
-   Para pausar el segmento actual, haga clic **en Pausar**.
-   Para detener el segmento actual, haga clic en **Detener**.
-   Para ir directamente a un archivo, haga doble clic en el elemento de la lista de reproducción.
-   Para eliminar un archivo de la lista de reproducción, seleccione el elemento de la lista de reproducción. A **continuación, seleccione Quitar de la lista de** reproducción en el **menú** Archivo.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location                                                     | Ruta de acceso o dirección URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [Windows SDK](https://www.microsoft.com/download/details.aspx?id=8279) | *Raíz del SDK* \\ Lista de \\ reproducción \\ de mediafoundation multimedia de \\ ejemplos |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de BasicPlayback](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Origen del secuenciador](sequencer-source.md)
</dt> </dl>

 

 
