---
description: Enumera y explica las responsabilidades de la GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilidades de la GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e4d2189d1d4258566a5e4baab357dc446a8f1c4ea409d7af328a85bf84c217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919043"
---
# <a name="responsibilities-of-the-gina"></a>Responsabilidades de la GINA

> [!Note]  
> Los archivos DLL de GINA se omiten Windows Vista.

 

Un archivo DLL [*de GINA*](../secgloss/g-gly.md) tiene las siguientes responsabilidades:

-   Supervisión de SAS

    GINA es responsable de reconocer una secuencia de atención [*segura*](../secgloss/s-gly.md) (SAS), supervisar los eventos de SAS y notificar a Winlogon cuando se ha producido una SAS. Tenga en cuenta que puede haber más de una SAS definida y el conjunto de SAS definidos puede cambiar con el tiempo. Por ejemplo, puede haber un conjunto de SAS cuando [*Winlogon*](../secgloss/w-gly.md) está en estado de apagado y otro conjunto cuando está en estado de sesión iniciada.

    Winlogon proporciona servicios para ayudar a la GINA a usar la SAS CTRL+ALT+SUPR.

-   Procesamiento de SAS

    Una razón para hacer que la GINA sea reemplazable es proporcionar mecanismos alternativos de identificación y autenticación. Para ello, el GINA debe presentar todas las interfaces de usuario resultantes del reconocimiento de una SAS. Cuando ningún usuario ha iniciado sesión, la GINA es responsable de presentar opciones de identificación y autenticación, así como cualquier otra opción permitida que no esté autenticada. Cuando un usuario inicia sesión, la GINA es responsable de presentar las opciones pertinentes al usuario, así como de realizar las acciones que considere adecuadas. Por ejemplo, en un sistema que incluye una tarjeta inteligente [*,*](../secgloss/s-gly.md)puede ser adecuado bloquear automáticamente la estación de trabajo si el usuario quita la tarjeta inteligente.

-   Activación del shell

    Cuando un usuario inicia sesión, la GINA es responsable de crear uno o varios procesos iniciales para ese usuario. (En esta documentación, se supone que estos procesos iniciales presentan una interfaz al usuario. Sin embargo, los procesos pueden ser realmente cualquier proceso y no necesariamente tienen que interactuar con el usuario). Estos procesos se conocen como el *shell de usuario* o simplemente el *shell*. Como parte de la activación del shell, el GINA debe asignar el token del usuario que acaba de iniciar sesión a los procesos. Winlogon proporciona un servicio para ayudar a la GINA a asignar el token.

 

 
