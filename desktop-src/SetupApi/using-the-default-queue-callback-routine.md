---
description: Se puede especificar la rutina de devolución de llamada de cola predeterminada para controlar las notificaciones enviadas por SetupCommitFileQueue, o bien una rutina de devolución de llamada personalizada que se basa en la funcionalidad de la rutina de devolución de llamada de cola predeterminada.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Usar la rutina de devolución de llamada de cola predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667183"
---
# <a name="using-the-default-queue-callback-routine"></a>Usar la rutina de devolución de llamada de cola predeterminada

Se puede especificar la rutina de devolución de llamada de cola predeterminada para controlar las notificaciones enviadas por [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), o bien una rutina de devolución de llamada personalizada que se basa en la funcionalidad de la rutina de devolución de llamada de cola predeterminada.

En las secciones siguientes se explica cómo inicializar y finalizar el contexto utilizado por una rutina de devolución de llamada de cola predeterminada. En las secciones también se describe cómo usar la rutina de devolución de llamada de cola predeterminada con [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) o una rutina de devolución de llamada personalizada.

-   [Inicialización y finalización del contexto de devolución de llamada](initializing-and-terminating-the-callback-context.md)
-   [Llamar a la rutina de devolución de llamada de cola predeterminada](calling-the-default-queue-callback-routine.md)

 

 



