---
description: La lista siguiente contiene los objetivos de diseño de TAPI MSP.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Objetivos de diseño generales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686982"
---
# <a name="general-design-goals"></a>Objetivos de diseño generales

La lista siguiente contiene los objetivos de diseño de TAPI MSP.

-   Las clases base se han mantenido simples, con los miembros y métodos introducidos solo cuando es absolutamente necesario.
-   Herencia simple. Sin herencia múltiple entre las clases, aunque se utiliza la herencia múltiple para las interfaces.
-   El bloqueo solo se produce en una dirección para evitar el interbloqueo. Los métodos del objeto de llamada que requieren el bloqueo en la llamada podrían llamar a métodos en la secuencia que requieren el bloqueo en la secuencia. Sin embargo, los métodos de la secuencia que requieren el bloqueo en la secuencia nunca llamarán a un método en la llamada que requiere un bloqueo en la llamada.
-   RefCounts se usan para proteger el acceso. Todas las devoluciones de llamada publicadas en el grupo de subprocesos contienen refCounts. El refcount se cancela cuando se cancela la espera. El objeto Address tiene refCounts en los terminales. Los objetos Call tienen refCounts en la dirección y en las secuencias. Los objetos de secuencia tienen refCounts en llamadas y terminales. Los terminales tienen refCounts en las secuencias. La refCounts circular se interrumpe cuando se llama al método shutdown en los objetos address y Call.

 

 



