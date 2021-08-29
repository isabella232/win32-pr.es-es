---
description: La lista siguiente contiene los objetivos de diseño de TAPI MSP.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Objetivos generales de diseño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984f897e5ad701e89c6ebf489ebd10828bf207e4f19ca186ca41e780b2e03cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140578"
---
# <a name="general-design-goals"></a>Objetivos generales de diseño

La lista siguiente contiene los objetivos de diseño de TAPI MSP.

-   Las clases base se han mantenido sencillas, con miembros y métodos introducidos solo cuando es absolutamente necesario.
-   Herencia simple. No hay herencia múltiple entre clases, aunque se usa la herencia múltiple para las interfaces.
-   El bloqueo solo se produce en una dirección para evitar el interbloqueo. Los métodos del objeto de llamada que requieren el bloqueo en la llamada pueden llamar a métodos de la secuencia que requieren el bloqueo en la secuencia. Sin embargo, los métodos de la secuencia que requieren el bloqueo en la secuencia nunca llamarán a un método en la llamada que requiera un bloqueo en la llamada.
-   Los recuentos de referencias se usan para proteger el acceso. Todas las devoluciones de llamada publicadas en el grupo de subprocesos mantienen recuentos de referencias. El recuento de referencias se cancela cuando se cancela la espera. El objeto Address tiene recuentos de referencias en terminales. Los objetos de llamada tienen recuentos de referencias en la dirección y en Secuencias. Los objetos de secuencia tienen recuentos de referencias en llamadas y terminales. Los terminales tienen recuentos de referencias en Secuencias. Los recuentos de referencias circulares se interrumpirán cuando se llame al método de apagado en los objetos Address y Call.

 

 



