---
title: Usar identificadores de contexto para mantener el estado en el servidor
description: Usar identificadores de contexto para mantener el estado en el servidor
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071378"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a>Usar identificadores de contexto para mantener el estado en el servidor

**Procedimiento recomendado:** Cada vez que el estado se mantiene en el servidor entre llamadas, use identificadores de contexto.

A menudo, los identificadores de contexto son de gran ayuda para los nuevos programadores de RPC y es posible que la sobrecarga de los identificadores de contexto de aprendizaje no parezca merecer la pena inicialmente. Merece la pena porque los identificadores de contexto tienen soluciones integradas para muchos problemas comunes detectados en la programación de red que, de lo contrario, tendrían que implementarse desde cero. Comprender los identificadores de contexto paga dividendos más adelante.

 

 




