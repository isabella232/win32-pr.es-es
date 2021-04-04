---
description: Se recomienda encarecidamente ejecutar la validación en cada paquete de instalación nuevo o recién modificado antes de intentar instalar el paquete por primera vez.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Validación de paquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908706"
---
# <a name="package-validation"></a>Validación de paquetes

Se recomienda encarecidamente ejecutar la validación en cada paquete de instalación nuevo o recién modificado antes de intentar instalar el paquete por primera vez.

La validación de paquetes incluye los tres procesos siguientes:

-   [Validación interna](internal-validation.md)
-   [Validación de grupo de cadenas](string-pool-validation.md)
-   [Evaluadores de coherencia interna-CIEM](internal-consistency-evaluators-ices.md)

Los módulos de combinación deben validarse mediante el método descrito en [validación de módulos de combinación](validating-merge-modules.md).

Evalcom2.dll proporciona un objeto COM que implementa las operaciones de validación para los paquetes de instalación y los módulos de combinación. El objeto principal implementa interfaces para programas de C/C++. Para obtener más información, vea automatización de la [validación](validation-automation.md).

 

 



