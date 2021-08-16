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
ms.openlocfilehash: 5df5b10ea6bd15ad083b26a61af037527f00576eaa6b7e1fa795ea1591417ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447025"
---
# <a name="to-set-input-settings"></a>Para establecer la entrada Configuración

Las propiedades básicas de los medios de entrada y los medios de secuencia se definen mediante la [**estructura WM \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Para los formatos de entrada, la aplicación establece la información del tipo de medio. En el caso de los formatos de secuencia, la información del tipo de medio se establece en el perfil que se asigna al escritor. Algunas propiedades son independientes del tipo de medio y deben establecerse para una entrada antes de comenzar la escritura. Estas propiedades son características de códec y escritor que son independientes del tipo de secuencia y se deben establecer después de asignar el perfil en el escritor, pero antes de comenzar la escritura.

Establecer una configuración de entrada requiere una llamada a [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). También puede comprobar el valor actual de una configuración con una llamada a [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Para el uso de perfiles con Writer**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> <dt>

[**Escribir imágenes Secuencias**](writing-image-streams.md)
</dt> </dl>

 

 




