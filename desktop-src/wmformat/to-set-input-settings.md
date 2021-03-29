---
title: Para establecer la configuración de entrada
description: Para establecer la configuración de entrada
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Advanced Systems Format (ASF), configuración de entrada
- ASF (formato de sistemas avanzados), configuración de entrada
- perfiles, configuración de entrada
- códecs, configuración de entrada
- flujos, configuración de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994957"
---
# <a name="to-set-input-settings"></a>Para establecer la configuración de entrada

La estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) define las propiedades básicas de los medios de entrada y de secuencia. En el caso de los formatos de entrada, la aplicación establece la información de tipo de medio. En el caso de los formatos de secuencia, la información de tipo de medio se establece en el perfil que se asigna al escritor. Algunas propiedades son independientes del tipo de medio y se deben establecer para una entrada antes de comenzar la escritura. Estas propiedades son características de códec y escritor que son independientes del tipo de secuencia y deben establecerse después de que el perfil se haya asignado en el escritor, pero antes de que empiece la escritura.

Establecer una configuración de entrada requiere una llamada a [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). También puede comprobar el valor actual de una configuración con una llamada a [**IWMWriterAdvanced2:: GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Para el uso de perfiles con Writer**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> <dt>

[**Escribir secuencias de imagen**](writing-image-streams.md)
</dt> </dl>

 

 




