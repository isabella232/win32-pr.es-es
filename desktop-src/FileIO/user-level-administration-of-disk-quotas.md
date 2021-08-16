---
description: Cómo obtener más espacio libre en disco después de superar la asignación de cuota.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Administración de cuotas de disco en el nivel de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214f1fb915d199ff6db3a6b3084c5c0f6f2df5c9737290fbdaa0e977a1163f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914365"
---
# <a name="user-level-administration-of-disk-quotas"></a>Administración de cuotas de disco en el nivel de usuario

Las cuotas de disco son transparentes para el usuario. Cuando un usuario pregunta cuánto espacio está disponible en un disco, el sistema notifica solo la asignación de cuota disponible que el usuario tiene disponible. Si el usuario supera esta asignación, el sistema devuelve el error **ERROR \_ DISK \_ FULL,** igual que lo haría para indicar que el disco estaba lleno.

Para obtener más espacio libre en disco después de superar la asignación de cuota, el usuario debe realizar una de las siguientes acciones:

-   Elimine algunos archivos.
-   Hacer que otro usuario reclame la propiedad de algunos archivos.
-   Hacer que el administrador aumente la asignación de cuota.

Los programas que necesitan recuperar la cantidad real de espacio libre en disco pueden llamar a la función [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) y ver el *parámetro TotalNumberOfFreeBytes.*

 

 



