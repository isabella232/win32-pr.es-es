---
title: Controles de contenedor
description: Controles de contenedor
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487055"
---
# <a name="container-controls"></a>Controles de contenedor

Como se describió anteriormente, los controles de contenedor son controles ActiveX que contienen visualmente otros controles. La arquitectura de controles ActiveX especifica la interfaz [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para habilitar los controles de contenedor. Los contenedores también pueden admitir controles de contenedor sin admitir **ISimpleFrameSite**, aunque no se puede garantizar el comportamiento. Por esta razón, existe una categoría de componentes para los controles SimpleFrameSite donde se requiere la funcionalidad completa de esta interfaz.

Para admitir controles de contenedor sin implementar [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), un contenedor de controles ActiveX debe:

-   Active todos los controles en todo momento.
-   Reparent los controles contenidos al hWnd del control que lo contiene.
-   Permanece el elemento primario del control contenedor.

 

 




