---
title: Llamadas anidadas a SRSetRestorePoint
description: En este tema se describe la compatibilidad con llamadas anidadas a SRSetRestorePoint a través de los \_ tipos de eventos Begin Nested \_ System Change \_ y end \_ Nested \_ System \_ Change.
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268878"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>Llamadas anidadas a SRSetRestorePoint

En este tema se describe la compatibilidad con llamadas anidadas a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) a través de los \_ tipos de eventos Begin Nested System Change \_ \_ y end \_ Nested \_ System \_ Change.

Las aplicaciones pueden llamar a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) con seguridad cuando se usan estos tipos de eventos. La primera llamada a la función crea un punto de restauración. Las llamadas anidadas subsiguientes a la función no crean puntos de restauración. Por ejemplo, supongamos que una aplicación realiza las siguientes llamadas a **SRSetRestorePoint**:<dl> Para el punto de restauración A con dwEventType = iniciar \_ cambio de sistema anidado \_ \_  
Para el punto de restauración B con dwEventType = BEGIN \_ Nested \_ System \_ Change  
Para el punto de restauración B con dwEventType = fin de \_ cambiar el sistema anidado \_ \_  
Para el punto de restauración A con dwEventType = fin de \_ \_ cambio del sistema anidado \_  
</dl>

La segunda llamada no crea un nuevo punto de restauración porque la llamada está anidada.

 

 




