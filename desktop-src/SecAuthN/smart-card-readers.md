---
description: Los lectores son dispositivos estándar en un sistema de tarjetas inteligentes. Se controlan a través de controladores y se introducen y quitan del sistema a través de Plug and Play o a través del elemento Panel de control Devices.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Lectores de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374935"
---
# <a name="smart-card-readers"></a>Lectores de tarjetas inteligentes

Los lectores son dispositivos estándar en un [*sistema de tarjetas inteligentes.*](../secgloss/s-gly.md) Se controlan a través de controladores y se introducen y quitan del sistema a través de Plug and Play o a través del elemento Panel de control Devices.

El subsistema de tarjeta inteligente debe definir cada lector [*para su uso.*](../secgloss/s-gly.md) El subsistema no es responsable de ningún lector que no se le ha dado específicamente.

Los lectores de tarjetas inteligentes se pueden dividir en grupos lógicos denominados grupos de lectores. El subsistema puede definir estos grupos, así como los administradores y los usuarios. Un lector puede pertenecer a más de un grupo de lectores

El subsistema de tarjeta inteligente define los grupos siguientes.



| Grupo                | Descripción                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCard$AllReaders     | Este grupo contiene todos los lectores del sistema. Un nuevo lector dado al subsistema de tarjetas inteligentes se incluye automáticamente en el grupo de lectores de todo el sistema, SCard$AllReaders.                         |
| SCard$DefaultReaders | Este grupo predeterminado, uno para cada [*terminal,*](../secgloss/t-gly.md)contiene todos los lectores asignados al terminal que no están reservados para un uso específico. |



 

 

 
