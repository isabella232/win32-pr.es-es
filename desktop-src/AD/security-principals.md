---
title: Entidades de seguridad
description: En Windows 2000, una entidad de seguridad es un usuario, un grupo o un equipo \ 8212; entidad que el sistema de seguridad reconoce.
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- AD de entidades de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877ed77b365fa4a61444e4936dbe859379ee397
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656215"
---
# <a name="security-principals"></a>Entidades de seguridad

En Windows 2000, una entidad de seguridad es un usuario, un grupo o un equipo, una entidad que el sistema de seguridad reconoce. Esto incluye a los usuarios humanos, así como a los procesos autónomos. En realidad, el sistema de seguridad no puede indicar la diferencia entre los usuarios que han iniciado sesión y los procesos que se ejecutan en el equipo. Ve ambos como entidades de seguridad con nombres de entidad de seguridad.

Los usuarios, los grupos y los equipos se crean y almacenan como objetos en Active Directory Domain Services. También hay entidades de seguridad conocidas que representan identidades especiales definidas por el sistema de seguridad de Windows 2000, como todos, sistema local, propio usuario principal, usuario autenticado, propietario del creador, etc. Los objetos que representan las entidades de seguridad conocidas, como el inicio de sesión anónimo, se almacenan en el contenedor de entidades de seguridad WellKnown bajo el contenedor de configuración.

 

 




