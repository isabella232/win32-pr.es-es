---
title: RAS AutoDial
description: Una característica denominada \ 0034;conexión predeterminada \ 0034; se agregó al sistema en Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- AutoDial, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7956148919505eb16d1fb2fe9bc045fa7ecbaa7e2959c430e15f8013ef372ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909875"
---
# <a name="ras-autodial"></a>RAS AutoDial

Se ha agregado al sistema una característica denominada "conexión predeterminada" en Windows XP. Si hay un intento de conexión con error, el sistema comprueba si hay una coincidencia explícita (para el nombre winsock o el nombre del recurso compartido) en la base de datos, si no es así, marca la conexión predeterminada si hay una.

**Windows 2000:** Cuando se produce un error al intentar conectarse a una dirección de red porque no se puede acceder al host, la característica AutoDial puede iniciar automáticamente una operación de conexión de acceso telefónico. Para ello, AutoDial busca en su base de datos de direcciones de red una entrada de la libreta de teléfonos que puede usar para establecer la conexión.

**Windows NT 4.0: ** RAS mantiene una base de datos de los nombres de Winsock o los nombres de recurso compartido a los que ha alcanzado correctamente mientras una conexión RAS/VPN estaba activa. Más adelante, cuando se produce un error en un intento de conexión winsock o share, el sistema comprueba esta base de datos y ofrece marcar automáticamente la conexión almacenada.

 

 




