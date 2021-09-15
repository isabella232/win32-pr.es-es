---
title: Para establecer la entrada Configuración
description: Para establecer la entrada Configuración
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Formato de sistemas avanzados (ASF), configuración de entrada
- ASF (formato de sistemas avanzados), configuración de entrada
- perfiles, configuración de entrada
- códecs, configuración de entrada
- streams,input settings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247244"
---
# <a name="to-set-input-settings"></a>Para establecer la entrada Configuración

Las propiedades básicas de los medios de entrada y los medios de secuencia se definen mediante la [**estructura WM \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Para los formatos de entrada, la aplicación establece la información del tipo de medio. Para los formatos de secuencia, la información del tipo de medio se establece en el perfil que asigna al escritor. Algunas propiedades son independientes del tipo de medio y se deben establecer para una entrada antes de comenzar la escritura. Estas propiedades son características de códec y escritor que son independientes del tipo de secuencia y deben establecerse después de asignar el perfil en el escritor, pero antes de comenzar la escritura.

Establecer una configuración de entrada requiere una llamada a [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). También puede comprobar el valor actual de una configuración con una llamada a [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Para el uso de perfiles con Writer**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> <dt>

[**Escribir imágenes Secuencias**](writing-image-streams.md)
</dt> </dl>

 

 




