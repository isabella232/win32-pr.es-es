---
description: Enumera y explica las responsabilidades de GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilidades de GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082610"
---
# <a name="responsibilities-of-the-gina"></a>Responsabilidades de GINA

> [!Note]  
> Los archivos dll de GINA se omiten en Windows Vista.

 

Un archivo dll de [*Gina*](../secgloss/g-gly.md) tiene las siguientes responsabilidades:

-   Supervisión de SAS

    GINA es responsable de reconocer una [*secuencia de atención segura*](../secgloss/s-gly.md) (SAS), la supervisión de eventos SAS y la notificación de Winlogon cuando se ha producido una SAS. Tenga en cuenta que puede haber más de una SAS definida, y el conjunto de SASs definido puede cambiar con el tiempo. Por ejemplo, puede haber un conjunto de SASs cuando [*Winlogon*](../secgloss/w-gly.md) está en el estado de cierre de sesión y otro conjunto cuando está en el estado de la sesión iniciada.

    Winlogon proporciona servicios para ayudar a GINA en el uso de las SA CTRL + ALT + SUPR.

-   Procesamiento de SAS

    Uno de los motivos para realizar la sustitución de GINA es proporcionar mecanismos de identificación y autenticación alternativos. Para ello, GINA debe presentar todas las interfaces de usuario que resultan del reconocimiento de una SAS. Cuando ningún usuario ha iniciado sesión, GINA es responsable de presentar las opciones de identificación y autenticación, así como cualquier otra opción permitida que no esté autenticada. Cuando un usuario ha iniciado sesión, GINA es responsable de presentar las opciones pertinentes al usuario, así como de tomar las medidas adecuadas. Por ejemplo, en un sistema que incluye una [*tarjeta inteligente*](../secgloss/s-gly.md), puede ser adecuado bloquear automáticamente la estación de trabajo si el usuario quita la tarjeta inteligente.

-   Activación de Shell

    Cuando un usuario inicia sesión, GINA es responsable de crear uno o más procesos iniciales para ese usuario. En esta documentación, se supone que estos procesos iniciales presentan una interfaz al usuario. Sin embargo, los procesos pueden ser realmente cualquier proceso y no tienen por qué interactuar con el usuario). Estos procesos se conocen como el *Shell de usuario* o simplemente el *Shell*. Como parte de la activación del shell, GINA debe asignar el token del usuario que acaba de iniciar sesión a los procesos. Winlogon proporciona un servicio que ayuda a GINA a asignar el token.

 

 
