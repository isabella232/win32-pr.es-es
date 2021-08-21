---
description: Notificación a CBasePin de cambios de estado de filtro
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notificación a CBasePin de cambios de estado de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7193402331f150f88217e2d200279e93314c40a9056f52bc31d8100106d4f960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153001"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Notificación a CBasePin de cambios de estado de filtro

La **clase CBasePin** se notifica cada vez que cambia el estado del filtro propietario. Para cada transición de estado, el filtro llama a un método correspondiente en el pin, como se muestra en la tabla siguiente.



| Nuevo estado de filtro | CBasePin (método)                                 |
|------------------|-------------------------------------------------|
| Detenido          | [**CBasePin::Inactive**](cbasepin-inactive.md) |
| En pausa           | [**CBasePin::Active**](cbasepin-active.md)     |
| En ejecución          | [**CBasePin::Run**](cbasepin-run.md)           |



 

La clase derivada debe invalidar estos métodos para responder al cambio de estado. Según el filtro, el pin podría iniciar un subproceso de trabajo que entregue ejemplos, confirme o desaproteja su asignador de memoria, etc.

 

 



