---
title: Obtención de información de configuración de secuencias de códecs
description: Obtención de información de configuración de secuencias de códecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- streams,configurations from codecs
- códecs, obtener configuraciones de flujo de
- streams,codec formats
- códecs, formatos
- streams,IWMCodecInfo (interfaz)
- IWMCodecInfo,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10cd131bfd263e0e9a0616b6fa9b59b3f3b03ace30a199b8b79f8b3c3f3f09f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433871"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>Obtención de información de configuración de secuencias de códecs

En el caso de las secuencias de audio y vídeo que usan los códecs Windows Media Audio y Video, debe obtener los valores de las estructuras de configuración de secuencia del códec que desea usar. Aunque es posible establecer estos valores usted mismo, el uso de los códecs garantiza que los valores sean precisos. No debe modificar los valores de estas estructuras a menos que la documentación recomiende específicamente un cambio determinado.

La información de los códecs tiene la forma de formatos de códec. Cada formato de códec es un formato de secuencia único admitido por el códec. Para obtener más información sobre los formatos de secuencia, vea [Formatos](formats.md).

Puede solicitar información de los códecs Windows Media mediante las interfaces [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)e [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) del objeto del administrador de perfiles. Para obtener la [**interfaz IWMProfileManager de**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) un objeto de administrador de perfiles, llame a la [**función WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) Llame **a QueryInterface** en **IWMProfileManager** para obtener **IWMCodecInfo3**.

En las secciones siguientes se describe cómo obtener la información que necesita.



| Sección                                                                                                | Descripción                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Para enumerar todos los códecs multimedia Windows instalados](to-enumerate-all-installed-windows-media-codecs.md) | Describe cómo usar los métodos de las interfaces **IWMCodecInfo** e **IWMCodecInfo2** para recuperar el nombre y el índice de códec de cada códec Windows media instalado. |
| [Para enumerar formatos de códec](to-enumerate-codec-formats.md)                                           | Describe cómo obtener objetos de configuración de secuencias de códecs para su uso en los perfiles.                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> </dl>

 

 




