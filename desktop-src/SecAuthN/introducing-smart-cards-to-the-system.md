---
description: Antes de que el subsistema de tarjeta inteligente pueda encontrar una tarjeta inteligente, la tarjeta inteligente debe incorporarse al sistema.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Presentación de tarjetas inteligentes en el sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278572"
---
# <a name="introducing-smart-cards-to-the-system"></a>Presentación de tarjetas inteligentes en el sistema

Antes de que el [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md) pueda encontrar una [*tarjeta inteligente*](../secgloss/s-gly.md), la tarjeta inteligente debe incorporarse al sistema. Normalmente, esto se realiza con una herramienta de configuración de tarjeta inteligente proporcionada por el fabricante de la tarjeta. La herramienta puede ser un programa en un disquete (con la tarjeta inteligente), un control ActiveX disponible en un sitio web, etc.

La herramienta de instalación debe proporcionar los siguientes datos sobre la tarjeta:

-   Su [*cadena ATR*](../secgloss/a-gly.md)y una máscara opcional que se usará como ayuda para identificar la tarjeta.
-   Una lista de interfaces de tarjeta inteligente que admite la tarjeta.
-   Nombre para mostrar de la tarjeta que se va a usar para identificar la tarjeta al usuario. En la mayoría de los casos, el usuario lo proporcionará a la herramienta de instalación.
-   [*Proveedor de servicios principal*](../secgloss/p-gly.md) asociado a la tarjeta (opcional) que se utilizará al obtener acceso a la tarjeta a través de interfaces com.

Para simplificar las herramientas de instalación y garantizar la integridad de la [*base de datos de tarjeta inteligente*](../secgloss/s-gly.md), el subsistema de tarjeta inteligente proporciona las dos funciones siguientes. [**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduce una tarjeta inteligente en la base de datos y [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) la quita de la base de datos.

 

 
