---
title: Marcado automático de RAS
description: Una característica denominada \ 0034; conexión predeterminada \ 0034; se agregó al sistema en Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- Marcado automático, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676247"
---
# <a name="ras-autodial"></a>Marcado automático de RAS

Se ha agregado una característica denominada "conexión predeterminada" al sistema en Windows XP. Si se produce un error en el intento de conexión, el sistema comprueba si hay una coincidencia explícita (para nombre Winsock o nombre de recurso compartido) en la base de datos si no es así, marca la conexión predeterminada en caso de que haya alguna.

**Windows 2000:** Cuando se produce un error al intentar conectarse a una dirección de red porque no se puede tener acceso al host, la característica de marcado automático puede iniciar automáticamente una operación de conexión de acceso telefónico. Para ello, el marcado automático busca en la base de datos de direcciones de red una entrada de libreta de teléfonos que pueda utilizar para establecer la conexión.

**Windows NT 4,0:  ** RAS mantiene una base de datos con los nombres de Winsock y/o los nombres de recursos compartidos que se han alcanzado correctamente mientras una conexión RAS/VPN estaba activa. Más adelante, cuando se produzca un error en un intento de conexión de Winsock o recurso compartido, el sistema comprobará esta base de datos y ofrecerá la marca de la conexión almacenada.

 

 




