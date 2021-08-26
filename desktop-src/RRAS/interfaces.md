---
title: Interfaces RAS
description: Una interfaz representa una red a la que se puede acceder a través de un adaptador LAN o WAN.
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef716e0db05fe37a0a7d326fbf5f8da878a0628d1deec9e996fcc49d917cc051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030145"
---
# <a name="ras-interfaces"></a>Interfaces RAS

Una interfaz representa una red a la que se puede acceder a través de un adaptador LAN o WAN. Cada interfaz tiene un identificador único en el enrutador. Las interfaces que están activas tienen un adaptador que proporciona conectividad a la red que representan. Las interfaces inactivas no tienen un adaptador que proporcione conectividad, a menos que un administrador deshabilite la interfaz después de que ya tuviera un adaptador.

El enrutamiento de un paquete a una red representada por una interfaz hará que el enrutador asigne un adaptador para esa interfaz y establezca una conexión WAN a la red remota. La asignación de un adaptador a una interfaz se conoce como *enlace*.

Las interfaces son objetos administrables. Cada interfaz aparece como una fila en la tabla de interfaz de la MIB de SNMP adecuada.