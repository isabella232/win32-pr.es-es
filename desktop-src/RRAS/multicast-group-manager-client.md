---
title: Cliente del administrador de grupo de multidifusión
description: Un cliente es una entidad que llama a una función MGM, como un protocolo de enrutamiento o una aplicación administrativa.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779602"
---
# <a name="multicast-group-manager-client"></a>Cliente del administrador de grupo de multidifusión

Un cliente es una entidad que llama a una función MGM, como un protocolo de enrutamiento o una aplicación administrativa.

La API MGM la usan principalmente los protocolos de enrutamiento de multidifusión. Los desarrolladores de protocolos de enrutamiento de multidifusión usan la API MGM para:

-   Mantener la pertenencia a grupos
-   Controlar la propiedad de la interfaz
-   Recibir notificaciones del administrador del grupo de multidifusión con respecto a otras solicitudes de protocolos de enrutamiento de multidifusión para datos de multidifusión

Las aplicaciones administrativas específicas que deben supervisar entradas de reenvío de multidifusión (MFEs) pueden hacerlo sin agregar ni quitar la pertenencia a grupos. Los desarrolladores de aplicaciones administrativas usan funciones MGM específicas para revisar la información en MFEs.

> [!Note]  
> Los protocolos de enrutamiento de multidifusión también tienen acceso a MFEs.

 

Un MFE es la información de reenvío que el administrador del grupo de multidifusión crea en función de la pertenencia a grupos. Los MFEs que se recuperan del administrador del grupo de multidifusión pueden proporcionar información estadística. Una aplicación administrativa puede usar esta información para determinar las acciones adecuadas. Por ejemplo, una aplicación administrativa podría realizar acciones basadas en el volumen de paquetes de una interfaz específica.

 

 




