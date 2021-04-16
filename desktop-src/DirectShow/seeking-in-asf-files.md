---
description: Buscar en archivos ASF
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Buscar en archivos ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e957fbdf7ed7df1a9cb38b14e39d384b15ab25b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537119"
---
# <a name="seeking-in-asf-files-directshow"></a>Buscar en archivos ASF (DirectShow)

El [lector ASF de WM](wm-asf-reader-filter.md), a través de su interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , puede realizar búsquedas temporales muy precisas en el contenido basado en Windows Media que tiene un índice temporal. (Todo el contenido indizado de Marcos también contiene un índice temporal). La búsqueda con precisión de fotogramas garantizada no se admite directamente en el lector ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad. En primer lugar, use el SDK de Windows Media Format directamente para crear una instancia del objeto lector sincrónico, abra el archivo, obtenga la marca de tiempo asociada a un marco especificado y, a continuación, use la interfaz **IMediaSeeking** de DirectShow para buscar en ese momento. La interfaz [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) no admite la búsqueda de contenido basado en Windows Media con precisión de fotogramas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



