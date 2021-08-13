---
description: Inicializar Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Inicializar Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202ab57db5821b252001a723eb8765493eb86362111da5c54e5e16e9fca4219a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268925"
---
# <a name="initializing-media-foundation"></a>Inicializar Media Foundation

Antes de usar Microsoft Media Foundation objetos o interfaces, debe llamar a la [**función MFStartup.**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Pase la constante **MF \_ VERSION**.


```C++
    hr = MFStartup(MF_VERSION);
```



La [**función MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) inicializa el Media Foundation plataforma. Si **MFStartup** devuelve MF E BAD STARTUP VERSION, significa que la aplicación se compiló con una versión de los encabezados Media Foundation que no coincide con los archivos DLL de Media Foundation del \_ \_ \_ \_ sistema.

Para cada llamada a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), la aplicación debe llamar a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).


```C++
MFShutdown();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation PLATFORM API](media-foundation-platform-apis.md)
</dt> </dl>

 

 



