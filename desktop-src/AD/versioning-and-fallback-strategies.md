---
title: Estrategias de control de versiones y de reserva
description: Cuando una aplicación detecta una actualización parcial mediante una de las técnicas anteriores o lee un conjunto de objetos cuya fecha efectiva no se ha alcanzado todavía, la aplicación debe tratar la situación correctamente.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- Control de versiones y estrategias de reserva AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903091"
---
# <a name="versioning-and-fallback-strategies"></a>Estrategias de control de versiones y de reserva

Cuando una aplicación detecta una actualización parcial mediante una de las técnicas anteriores o lee un conjunto de objetos cuya fecha efectiva no se ha alcanzado todavía, la aplicación debe tratar la situación correctamente. En algunas aplicaciones, la respuesta correcta es "revertir" a una versión anterior de los objetos en cuestión. Active Directory Domain Services no proporcionan una utilidad de control de versiones, las aplicaciones que quieran esta funcionalidad deben proporcionarlas. Los enfoques para el control de versiones incluyen mantener los valores de "última buena conocida" almacenados en caché localmente y almacenar varios conjuntos de objetos en el directorio, por ejemplo, en los contenedores "antiguos", "actual" y "nuevo". Muchos otros esquemas son posibles.

Las implementaciones deben tener cuidado para evitar consecuencias imprevistas. Solo se debe usar una versión anterior de los objetos cuando se detecta una actualización parcial o cuando los nuevos objetos todavía no son "efectivos". Al revertirse porque algo de la aplicación "no funciona" podría eludir la intención de un administrador. Por ejemplo, dos equipos que anteriormente podían comunicarse podrían no ser capaces de hacerlo debido a un cambio en la Directiva del Protocolo de seguridad de Internet (IPsec). Si esto es intencionado en parte del administrador, los sistemas afectados no deben revertir a la Directiva que les permitió comunicarse, ya que esto sería una brecha de seguridad.

 

 




