---
title: Conexión compartida a Internet
description: BITS puede forzar una conexión de acceso telefónico para las redes domésticas que usan el uso compartido de conexión a Internet de Microsoft si el uso compartido de conexiones está configurado para marcar el acceso cuando los equipos de la red acceden a Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8736144b74d12666c4a364ac5b644ead35f8d1ec28aa03926bb7b691c8218f3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588625"
---
# <a name="internet-connection-sharing"></a>Conexión compartida a Internet

BITS puede forzar una conexión de acceso telefónico para las redes domésticas que usan el uso compartido de conexión a Internet de Microsoft si el uso compartido de conexiones está configurado para marcar el acceso cuando los equipos de la red acceden a Internet. Para evitar una conexión de acceso telefónico forzada, deshabilite la opción Establecer una conexión de acceso telefónico cada vez que un equipo de mi red intente acceder **a Internet** en el equipo host de uso compartido de conexiones que comparte su conexión a Internet.

Los equipos conectados al equipo host de uso compartido de conexiones suponen que tienen una conexión de red, por lo que BITS intentará transferir archivos. Si la opción de acceso telefónico está deshabilitada en el equipo host y el equipo host no tiene una conexión activa, las transferencias producirán un error transitorio. BITS volverá a intentar las transferencias periódicamente.

 

 




