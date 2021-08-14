---
title: Priorización de secuencias
description: Priorización de secuencias
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows SDK de formato multimedia, priorización de secuencias
- Formato de sistemas avanzados (ASF), priorización de secuencias
- ASF (formato de sistemas avanzados), priorización de secuencias
- Windows SDK de formato multimedia, orden de prioridad para secuencias
- Formato de sistemas avanzados (ASF), orden de prioridad para secuencias
- ASF (formato de sistemas avanzados), orden de prioridad para las secuencias
- streams,prioritization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd34bab6a7957d7cbcdf97a78fc3d8be1f663d43ef1eb1ec8d4c575571ad0a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197281"
---
# <a name="stream-prioritization"></a>Priorización de secuencias

Al crear un archivo ASF, puede especificar un orden de prioridad para sus flujos constituyentes. Si transmite un archivo con prioridad y el ancho de banda disponible no es suficiente para entregar todas las secuencias, el lector quitará los flujos en orden de prioridad inversa. De este modo, puede garantizar que las secuencias más importantes del archivo no se descartarán debido a dificultades de red.

La priorización de secuencias se configura con un objeto de priorización de secuencias y se agrega al perfil. Un perfil solo puede contener un objeto de priorización de secuencias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[**IWMProfile3::RemoveStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[**IWMStreamPrioritization (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[**Uso de la priorización de secuencias**](using-stream-prioritization.md)
</dt> </dl>

 

 




