---
description: Los lectores son dispositivos estándar en un sistema de tarjeta inteligente. Se controlan a través de controladores y se introducen y se quitan del sistema a través de Plug and Play o a través del elemento dispositivos del panel de control.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Lectores de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652934"
---
# <a name="smart-card-readers"></a>Lectores de tarjetas inteligentes

Los lectores son dispositivos estándar en un sistema de [*tarjeta inteligente*](../secgloss/s-gly.md) . Se controlan a través de controladores y se introducen y se quitan del sistema a través de Plug and Play o a través del elemento dispositivos del panel de control.

Cada lector debe definirse para que lo use el [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md). El subsistema no es responsable de ningún lector que no se haya asignado específicamente a él.

Los lectores de tarjetas inteligentes se pueden dividir en grupos lógicos denominados grupos de lector. El subsistema puede definir estos grupos, así como definidos por los administradores y los usuarios. Un lector puede pertenecer a más de un grupo de lectores

El subsistema de tarjeta inteligente define los siguientes grupos.



| Grupo                | Descripción                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PPAC $ AllReaders     | Este grupo contiene todos los lectores del sistema. Un nuevo lector proporcionado al subsistema de tarjeta inteligente se incluye automáticamente en el grupo de lectores de todo el sistema, PPAC $ AllReaders.                         |
| PPAC $ DefaultReaders | Este grupo predeterminado, uno para cada [*terminal*](../secgloss/t-gly.md), contiene todos los lectores asignados al terminal que no están reservados para uso específico. |



 

 

 
