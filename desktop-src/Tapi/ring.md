---
description: Un solo teléfono puede sonar con distintos modos de anillo.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: En anillo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001925"
---
# <a name="ring"></a>En anillo

Un solo teléfono puede sonar con distintos modos de anillo. Dada la amplia variedad de modos de anillo disponibles, los modos de anillo se identifican por medio de su número de modo de anillo. Un número de modo de anillo oscila entre cero y el número de modos de anillo disponibles menos uno.

Las funciones que utiliza una aplicación para controlar los modos de anillo de un dispositivo telefónico son [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), que suena un dispositivo telefónico abierto según un modo de anillo determinado y [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), que devuelve el modo de anillo actual de un dispositivo telefónico abierto.

Cuando se cambia el modo de anillo de un dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado. Los parámetros de este mensaje proporcionan una indicación del cambio.

 

 



