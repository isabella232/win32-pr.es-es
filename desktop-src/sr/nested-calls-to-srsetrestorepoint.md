---
title: Llamadas anidadas a SRSetRestorePoint
description: En este tema se describe la compatibilidad con llamadas anidadas a SRSetRestorePoint a través de los tipos de eventos BEGIN NESTED SYSTEM CHANGE y \_ \_ END NESTED SYSTEM \_ \_ \_ \_ CHANGE.
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12286a69bdb83cb5fd119280e8996c6612e359bf93b9371b6a088a98bf6fd881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857640"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>Llamadas anidadas a SRSetRestorePoint

En este tema se describe la compatibilidad con llamadas anidadas a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) a través de los tipos de eventos BEGIN NESTED SYSTEM CHANGE y \_ END NESTED SYSTEM \_ \_ \_ \_ \_ CHANGE.

Las aplicaciones pueden llamar a [**SRSetRestorePoint de forma segura**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) cuando se usan estos tipos de eventos. La primera llamada a la función crea un punto de restauración. Las llamadas anidadas posteriores a la función no crean puntos de restauración. Por ejemplo, suponga que una aplicación realiza las siguientes llamadas a **SRSetRestorePoint**:<dl> Para el punto de restauración A con dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ CHANGE  
Para el punto de restauración B con dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ CHANGE  
Para el punto de restauración B con dwEventType = END \_ NESTED \_ SYSTEM \_ CHANGE  
Para el punto de restauración A con dwEventType = END \_ NESTED \_ SYSTEM \_ CHANGE  
</dl>

La segunda llamada no crea un nuevo punto de restauración porque la llamada está anidada.

 

 




