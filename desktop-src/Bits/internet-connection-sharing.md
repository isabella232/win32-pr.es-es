---
title: Conexión compartida a Internet
description: BITS puede forzar una conexión de acceso telefónico para las redes domésticas que usan conexión compartida a Internet de Microsoft si la conexión compartida está configurada para marcar cuando los equipos de la red acceden a Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773375"
---
# <a name="internet-connection-sharing"></a>Conexión compartida a Internet

BITS puede forzar una conexión de acceso telefónico para las redes domésticas que usan conexión compartida a Internet de Microsoft si la conexión compartida está configurada para marcar cuando los equipos de la red acceden a Internet. Para evitar una conexión de acceso telefónico forzada, deshabilite la opción **establecer una conexión de acceso telefónico cada vez que un equipo en la red intente tener acceso a Internet** en el equipo host de conexión compartida que comparte su conexión a Internet.

Los equipos conectados al equipo host de conexión compartida suponen que tienen una conexión de red, por lo que BITS intentará transferir los archivos. Si la opción de acceso telefónico está deshabilitada en el equipo host y el equipo host no tiene una conexión activa, se producirá un error transitorio en las transferencias. BITS reintentará las transferencias periódicamente.

 

 




