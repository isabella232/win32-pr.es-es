---
title: Cliente del Administrador de grupos de multidifusión
description: Un cliente es una entidad que llama a una función MGM, como un protocolo de enrutamiento o una aplicación administrativa.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2fceda28404e20be5d2c3192b672b1d4e20cb1f95f238f8b561a989c564f6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790429"
---
# <a name="multicast-group-manager-client"></a>Cliente del Administrador de grupos de multidifusión

Un cliente es una entidad que llama a una función MGM, como un protocolo de enrutamiento o una aplicación administrativa.

Los protocolos de enrutamiento de multidifusión usan principalmente la API de MGM. Los desarrolladores de protocolos de enrutamiento de multidifusión usan la API de MGM para:

-   Mantener la pertenencia a grupos
-   Control de la propiedad de la interfaz
-   Recibir notificaciones del administrador de grupos de multidifusión relacionadas con las solicitudes de otros protocolos de enrutamiento de multidifusión para datos de multidifusión

Las aplicaciones administrativas específicas que deben supervisar las entradas de reenvío de multidifusión (MFE) pueden hacerlo sin agregar o quitar la pertenencia a grupos. Los desarrolladores de aplicaciones administrativas usan funciones específicas de MGM para revisar la información de las mfes.

> [!Note]  
> Los protocolos de enrutamiento de multidifusión también acceden a las MFE.

 

Un MFE reenvía información que el administrador de grupos de multidifusión crea en función de la pertenencia a grupos. Las MFE que se recuperan del administrador de grupos de multidifusión pueden proporcionar información estadística. Después, una aplicación administrativa puede usar esta información para determinar las acciones adecuadas. Por ejemplo, una aplicación administrativa podría realizar acciones basadas en el volumen de paquetes en una interfaz específica.

 

 




