---
title: Obtención de información de configuración de la secuencia de códecs
description: Obtención de información de configuración de la secuencia de códecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- flujos, configuraciones de códecs
- códecs, obtener configuraciones de secuencia de
- secuencias, formatos de códecs
- códecs, formatos
- streams, interfaz IWMCodecInfo
- IWMCodecInfo, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104420435"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>Obtención de información de configuración de la secuencia de códecs

En el caso de las secuencias de audio y vídeo que usan los códecs de Windows Media Audio y vídeo, debe obtener los valores de las estructuras de configuración de la secuencia del códec que desee usar. Aunque es posible establecer estos valores personalmente, el uso de los códecs garantiza que los valores sean precisos. No debe modificar los valores de estas estructuras a menos que la documentación recomiende específicamente un cambio determinado.

La información de los códecs tiene formato de códec. Cada formato de códec es un formato de flujo único compatible con el códec. Para obtener más información sobre los formatos de secuencias, vea [formatos](formats.md).

Puede solicitar información de los códecs de Windows Media con las interfaces [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)y [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) del objeto de administrador de perfiles. Para obtener la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) de un objeto de administrador de perfiles, llame a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) . Llame a **QueryInterface** en **IWMProfileManager** para obtener **IWMCodecInfo3**.

En las secciones siguientes se describe cómo obtener la información que necesita.



| Sección                                                                                                | Descripción                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Para enumerar todos los códecs de Windows Media instalados](to-enumerate-all-installed-windows-media-codecs.md) | Describe cómo usar los métodos de las interfaces **IWMCodecInfo** y **IWMCodecInfo2** para recuperar el nombre y el índice de códec de cada códec de Windows Media instalado. |
| [Para enumerar formatos de códecs](to-enumerate-codec-formats.md)                                           | Describe cómo obtener objetos de configuración de secuencia a partir de códecs para su uso en los perfiles.                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> </dl>

 

 




