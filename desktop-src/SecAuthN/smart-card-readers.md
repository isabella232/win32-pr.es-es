---
description: Los lectores son dispositivos estándar en un sistema de tarjetas inteligentes. Se controlan mediante controladores y se introducen en el sistema y se quitan del sistema mediante Plug and Play o a través del elemento Panel de control Dispositivos.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Lectores de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335aabe1d815e9b6d41ccfd820242209da63134797595d8a1c85f009f8551b7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917754"
---
# <a name="smart-card-readers"></a>Lectores de tarjetas inteligentes

Los lectores son dispositivos estándar en un [*sistema de tarjetas inteligentes.*](../secgloss/s-gly.md) Se controlan mediante controladores y se introducen en el sistema y se quitan del sistema mediante Plug and Play o a través del elemento Panel de control Dispositivos.

El subsistema de tarjeta inteligente debe definir cada lector [*para su uso.*](../secgloss/s-gly.md) El subsistema no es responsable de ningún lector que no se le ha dado específicamente.

Los lectores de tarjetas inteligentes se pueden dividir en grupos lógicos denominados grupos de lectores. El subsistema puede definir estos grupos, así como los administradores y los usuarios. Un lector puede pertenecer a más de un grupo de lectores

El subsistema de tarjeta inteligente define los grupos siguientes.



| Grupo                | Descripción                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCard$AllReaders     | Este grupo contiene todos los lectores del sistema. Un nuevo lector dado al subsistema de tarjetas inteligentes se incluye automáticamente en el grupo de lectores de todo el sistema, SCard$AllReaders.                         |
| SCard$DefaultReaders | Este grupo predeterminado, uno para cada [*terminal,*](../secgloss/t-gly.md)contiene todos los lectores asignados al terminal que no están reservados para un uso específico. |



 

 

 
