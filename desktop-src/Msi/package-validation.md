---
description: Se recomienda encarecidamente que ejecute la validación en todos los paquetes de instalación nuevos o recién modificados antes de intentar instalar el paquete por primera vez.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Validación de paquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250946"
---
# <a name="package-validation"></a>Validación de paquetes

Se recomienda encarecidamente que ejecute la validación en todos los paquetes de instalación nuevos o recién modificados antes de intentar instalar el paquete por primera vez.

La validación de paquetes incluye los tres procesos siguientes:

-   [Validación interna](internal-validation.md)
-   [Validación de grupo de cadenas](string-pool-validation.md)
-   [Evaluadores de coherencia internos: TIC](internal-consistency-evaluators-ices.md)

Los módulos de combinación se deben validar mediante el método descrito en [Validación de módulos de mezcla.](validating-merge-modules.md)

Evalcom2.dll proporciona un objeto COM que implementa operaciones de validación para paquetes de instalación y módulos de combinación. El objeto principal implementa interfaces para programas de C/C++. Para obtener más información, vea [Automatización de la validación.](validation-automation.md)

 

 



