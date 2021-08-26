---
title: Controles de contenedor
description: Controles de contenedor
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82048c02c6aa1db020a030f9a5a2fc92f0c5fc08914c930a315a97b31a88c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896445"
---
# <a name="container-controls"></a>Controles de contenedor

Como se describió anteriormente, los controles de contenedor ActiveX controles que contienen visualmente otros controles. La arquitectura ActiveX controles especifica la [**interfaz ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para habilitar los controles de contenedor. Los contenedores también pueden admitir controles de contenedor **sin admitir ISimpleFrameSite,** aunque no se puede garantizar el comportamiento. Por esta razón, existe una categoría de componente para los controles SimpleFrameSite donde se requiere toda la funcionalidad de esta interfaz.

Para admitir controles de contenedor sin implementar [**ISimpleFrameSite,**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)ActiveX contenedor de controles debe:

-   Active todos los controles en todo momento.
-   Vuelva a tener en cuenta los controles contenidos en el hWnd del control que lo contiene.
-   Siga siendo el elemento primario del control contenedor.

 

 




