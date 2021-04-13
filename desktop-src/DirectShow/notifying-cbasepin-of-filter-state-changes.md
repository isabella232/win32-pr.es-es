---
description: Notificar los cambios de estado de filtro de CBasePin
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notificar los cambios de estado de filtro de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359949"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a>Notificar los cambios de estado de filtro de CBasePin

La clase **CBasePin** se notifica cada vez que cambia el estado del filtro propietario. Para cada transición de estado, el filtro llama al método correspondiente en el código PIN, como se muestra en la tabla siguiente.



| Nuevo estado de filtro | Método CBasePin                                 |
|------------------|-------------------------------------------------|
| Detenido          | [**CBasePin:: inactivo**](cbasepin-inactive.md) |
| En pausa           | [**CBasePin:: Active**](cbasepin-active.md)     |
| En ejecución          | [**CBasePin:: Run**](cbasepin-run.md)           |



 

La clase derivada debe invalidar estos métodos para responder al cambio de estado. Dependiendo del filtro, el pin puede iniciar un subproceso de trabajo que entregue ejemplos, confirme o desconfirme su asignador de memoria, etc.

 

 



