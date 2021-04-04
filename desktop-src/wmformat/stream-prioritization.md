---
title: Priorización de flujos
description: Priorización de flujos
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK, priorización de flujos
- Advanced Systems Format (ASF), priorización de flujos
- ASF (formato de sistemas avanzados), priorización de flujo
- SDK de Windows Media Format, orden de prioridad para secuencias
- Advanced Systems Format (ASF), orden de prioridad de las secuencias
- ASF (formato de sistemas avanzados), orden de prioridad para flujos
- flujos, priorización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077332"
---
# <a name="stream-prioritization"></a>Priorización de flujos

Al crear un archivo ASF, puede especificar un orden de prioridad para sus flujos constituyentes. Si transmite por secuencias un archivo con prioridad y el ancho de banda disponible no es suficiente para ofrecer todas las secuencias, el lector quitará los flujos en orden de prioridad inverso. De este modo, puede garantizar que las secuencias más importantes del archivo no se quitarán debido a problemas de red.

La priorización de flujo se configura con un objeto de priorización de flujo y se agrega al perfil. Un perfil puede contener solo un objeto de priorización de flujo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[**IWMProfile3::RemoveStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[**Interfaz IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[**Usar la priorización de flujos**](using-stream-prioritization.md)
</dt> </dl>

 

 




