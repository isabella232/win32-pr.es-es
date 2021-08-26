---
description: Para que el subsistema de tarjetas inteligentes pueda encontrar una tarjeta inteligente, la tarjeta inteligente debe introducirse en el sistema.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Introducción a las tarjetas inteligentes en el sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07cd65135e1580792135a1042729f2002f4437697fa0548a4f6cd776650485b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015715"
---
# <a name="introducing-smart-cards-to-the-system"></a>Introducción a las tarjetas inteligentes en el sistema

Para que [*el subsistema de tarjeta*](../secgloss/s-gly.md) inteligente pueda encontrar una tarjeta [*inteligente,*](../secgloss/s-gly.md)debe introducirse en el sistema. Esto suele hacerse con una herramienta de configuración de tarjeta inteligente proporcionada por el fabricante de la tarjeta. La herramienta podría ser un programa en un disquete (con la tarjeta inteligente), un control de ActiveX disponible en un sitio web, y así sucesivamente.

La herramienta de instalación debe proporcionar los siguientes fragmentos de información sobre la tarjeta:

-   Su [*cadena ATR*](../secgloss/a-gly.md)y una máscara opcional que se usará como ayuda para identificar la tarjeta.
-   Lista de interfaces de tarjeta inteligente compatibles con la tarjeta.
-   Nombre para mostrar de la tarjeta que se usará para identificar la tarjeta al usuario. En la mayoría de los casos, el usuario lo suministrará a la herramienta de instalación.
-   Proveedor [*de servicios principal*](../secgloss/p-gly.md) asociado a la tarjeta (opcional) que se usará al acceder a la tarjeta a través de interfaces COM.

Para simplificar las herramientas de configuración y garantizar la integridad de la base de datos de [*tarjetas*](../secgloss/s-gly.md)inteligentes, el subsistema de tarjetas inteligentes proporciona las dos funciones siguientes. [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduce una tarjeta inteligente en la base de datos y [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) la quita de la base de datos.

 

 
