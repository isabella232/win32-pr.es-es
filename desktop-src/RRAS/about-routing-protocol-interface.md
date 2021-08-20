---
title: Acerca de la interfaz de protocolo de enrutamiento
description: En la siguiente documentación se describe la integración de protocolos de enrutamiento de terceros en el Servicio de enrutamiento y acceso remoto (RRAS).
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- RRAS del servicio de enrutamiento y acceso remoto, interfaz de protocolo de enrutamiento
- RRAS del servicio de enrutamiento y acceso remoto, interfaz de protocolo de enrutamiento, descrito
- RRAS de la interfaz de protocolo de enrutamiento
- RRAS de la interfaz de protocolo de enrutamiento , descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76689e0e7ca40c2677491fc0673c596c902a73ee85b677161c208fe71d090367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792122"
---
# <a name="about-routing-protocol-interface"></a>Acerca de la interfaz de protocolo de enrutamiento

En la siguiente documentación se describe la integración de protocolos de enrutamiento de terceros en el Servicio de enrutamiento y acceso remoto (RRAS). RRAS es una característica de Windows que actúa como enrutador multi protocolo. RRAS define la interfaz entre el administrador de enrutadores y el protocolo de enrutamiento. El protocolo de enrutamiento se implementa en una biblioteca de vínculos dinámicos (DLL).

Use esta interfaz para implementar protocolos de enrutamiento, como IGRP, NLSP y BGP, como archivos DLL en modo de usuario que funcionan con RRAS.

En esta documentación se describen los temas siguientes:

-   [Adaptadores](adapters.md)
-   [Interfaces](interfaces.md)
-   [Rutas estáticas y autostáticas](static-and-autostatic-routes.md)

 

 




