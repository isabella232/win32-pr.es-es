---
description: Una interfaz de tarjeta inteligente consta de un conjunto predefinido de servicios disponibles dentro de una tarjeta inteligente, los protocolos necesarios para invocar los servicios y cualquier suposición relacionada con el contexto de los servicios.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfaces de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374939"
---
# <a name="smart-card-interfaces"></a>Interfaces de tarjeta inteligente

Una [*interfaz de*](../secgloss/s-gly.md) tarjeta inteligente consta de un conjunto predefinido de servicios disponibles dentro de una tarjeta inteligente, los protocolos necesarios para invocar los servicios y cualquier suposición con respecto al contexto de los servicios. 

Con respecto a las tarjetas inteligentes, el término "interfaz" es similar a cómo se usa en COM, que a su vez es similar en concepto al identificador de aplicación ISO 7816/5, pero con un ámbito diferente.

Cada interfaz de tarjeta inteligente se identifica mediante un GUID. Por ejemplo, se podría definir una interfaz que proporciona información biorritm a su titular. Si una tarjeta inteligente determinada admite este servicio, puede reclamar que admita ese GUID de interfaz. Con los GUID de interfaz, una aplicación puede buscar un conjunto determinado de interfaces, localizando cualquier tarjeta que admita ese conjunto, para completar una tarea.

Aunque una interfaz tiene un GUID, podría implementarse de forma diferente en distintas tarjetas. Por ejemplo, la interfaz biorhythm mencionada anteriormente puede tener varias implementaciones diferentes, pero se hace referencia a todas con el mismo GUID. Las distintas implementaciones no cambiarían la interacción entre la aplicación y la tarjeta inteligente. sin embargo, la interacción entre el [*proveedor de servicios*](../secgloss/c-gly.md) y las tarjetas inteligentes puede variar en función de la implementación de la interfaz.

El conjunto de interfaces compatibles con una tarjeta inteligente se define durante la introducción a la tarjeta inteligente (consulte Introducción a las tarjetas [inteligentes en el sistema).](introducing-smart-cards-to-the-system.md)

 

 
