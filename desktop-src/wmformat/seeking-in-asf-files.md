---
title: Buscar en archivos ASF (Windows Media Format 11 SDK)
description: Buscar en archivos ASF
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- SDK de Windows Media Format, buscar en archivos ASF
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), buscar
- ASF (formato de sistemas avanzados), búsqueda
- DirectShow, buscar en archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18389ded80f0202564cba0ce6384b5ff02d26fdd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078697"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Buscar en archivos ASF (Windows Media Format 11 SDK)

El [lector ASF de WM](wm-asf-reader-filter.md), a través de su interfaz **IMediaSeeking** , puede realizar búsquedas temporales muy precisas en el contenido basado en Windows Media que tiene un índice temporal. (Todo el contenido indizado de Marcos también contiene un índice temporal). La búsqueda con precisión de fotogramas garantizada no se admite directamente en el lector ASF de WM, pero hay una manera de hacerlo si necesita esta funcionalidad. En primer lugar, use el SDK de Windows Media Format directamente para crear una instancia del objeto lector sincrónico, abra el archivo, obtenga la marca de tiempo asociada a un marco especificado y, a continuación, use la interfaz **IMediaSeeking** de DirectShow para buscar en ese momento. La interfaz **IVideoFrameStep** de DirectShow no admite la búsqueda de contenido basado en Windows Media con precisión de fotogramas. En el ejemplo DSSeekFm del SDK de Windows Media Format se muestra cómo realizar búsquedas con precisión de fotogramas mediante el lector ASF de WM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Filtro de lector ASF de WM**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




