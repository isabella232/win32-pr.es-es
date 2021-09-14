---
description: Para que el subsistema de tarjetas inteligentes pueda encontrar una tarjeta inteligente, la tarjeta inteligente debe introducirse en el sistema.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Introducción a las tarjetas inteligentes en el sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071276"
---
# <a name="introducing-smart-cards-to-the-system"></a>Introducción a las tarjetas inteligentes en el sistema

Para que [*el subsistema de tarjeta*](../secgloss/s-gly.md) inteligente pueda encontrar una tarjeta [*inteligente,*](../secgloss/s-gly.md)debe introducirse en el sistema. Esto suele hacerse con una herramienta de configuración de tarjeta inteligente proporcionada por el fabricante de la tarjeta. La herramienta podría ser un programa en un disquete (con la tarjeta inteligente), un control ActiveX disponible en un sitio web, y así sucesivamente.

La herramienta de instalación debe proporcionar los siguientes fragmentos de información sobre la tarjeta:

-   Su [*cadena ATR*](../secgloss/a-gly.md)y una máscara opcional que se usará como ayuda para identificar la tarjeta.
-   Lista de interfaces de tarjeta inteligente compatibles con la tarjeta.
-   Nombre para mostrar de la tarjeta que se usará para identificar la tarjeta al usuario. En la mayoría de los casos, el usuario lo suministrará a la herramienta de instalación.
-   Proveedor [*de servicios principal*](../secgloss/p-gly.md) asociado a la tarjeta (opcional) que se usará al acceder a la tarjeta a través de interfaces COM.

Para simplificar las herramientas de configuración y garantizar la integridad de la base de datos de [*tarjetas*](../secgloss/s-gly.md)inteligentes, el subsistema de tarjetas inteligentes proporciona las dos funciones siguientes. [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduce una tarjeta inteligente en la base de datos y [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) la quita de la base de datos.

 

 
