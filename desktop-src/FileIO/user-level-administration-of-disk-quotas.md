---
description: Cómo obtener más espacio libre en disco después de superar la asignación de cuota.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Administración de las cuotas de disco en el nivel de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668366"
---
# <a name="user-level-administration-of-disk-quotas"></a>Administración de las cuotas de disco en el nivel de usuario

Las cuotas de disco son transparentes para el usuario. Cuando un usuario pregunta cuánto espacio hay disponible en un disco, el sistema solo notifica la concesión de cuota disponible que el usuario tiene disponible. Si el usuario supera esta asignación, el sistema devuelve el error de **\_ disco \_ lleno** , del mismo modo que indicaría que el disco estaba lleno.

Para obtener más espacio libre en disco después de superar la asignación de cuota, el usuario debe realizar una de las siguientes acciones:

-   Elimine algunos archivos.
-   Haga que otro usuario reclame la propiedad de algunos archivos.
-   Haga que el administrador aumente la concesión de cuota.

Los programas que necesitan recuperar la cantidad real de espacio libre en disco pueden llamar a la función [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) y examinar el parámetro *TotalNumberOfFreeBytes* .

 

 



