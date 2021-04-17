---
description: Los terminales conectables permiten a una aplicación crear terminales durante el tiempo de ejecución.
ms.assetid: 34ba4f3c-0a14-4705-9490-817c70700746
title: Terminales conectables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52802d98d7eb6985dbb7de9ca3facab90a5550e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688146"
---
# <a name="pluggable-terminals"></a>Terminales conectables

Los terminales conectables permiten a una aplicación crear terminales durante el tiempo de ejecución. Normalmente, los terminales se crean y controlan mediante un par proveedor de servicios de telefonía/proveedor de servicios multimedia (TSP/MSP), y esto sigue siendo el medio más versátil y estable de manipular los terminales. Sin embargo, algunas aplicaciones deben usar terminales simples en situaciones en las que no haya disponible un par de TSP/MSP adecuado. Solo los escritores de aplicaciones que estén familiarizados con las operaciones de TSP y MSP deben usar terminales conectables.

En la versión 3,1 de TAPI, los terminales conectables se agregan al modelo de TAPI. Los terminales conectables permiten a un tercero agregar un nuevo objeto de terminal que puede usar cualquier MSP.

Consulte [registro de terminales conectables](pluggable-terminal-registration.md) y [escritura de un terminal acoplable](writing-a-pluggable-terminal.md) para obtener más información.

 

 



