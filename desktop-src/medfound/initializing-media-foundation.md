---
description: Inicializar Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Inicializar Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678647"
---
# <a name="initializing-media-foundation"></a>Inicializar Media Foundation

Antes de usar cualquier objeto o interfaz de Microsoft Media Foundation, debe llamar a la función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Pase la **\_ versión** de la constante MF.


```C++
    hr = MFStartup(MF_VERSION);
```



La función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) inicializa la plataforma Media Foundation. Si **MFStartup** devuelve la \_ \_ \_ versión de inicio incorrecta MF E \_ , significa que la aplicación se compiló con una versión de los media Foundation encabezados que no coinciden con los media Foundation dll del sistema.

Para cada llamada a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), la aplicación debe llamar a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).


```C++
MFShutdown();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[API de Media Foundation Platform](media-foundation-platform-apis.md)
</dt> </dl>

 

 



