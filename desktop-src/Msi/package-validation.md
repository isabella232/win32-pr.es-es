---
description: Se recomienda encarecidamente que ejecute la validación en todos los paquetes de instalación nuevos o recién modificados antes de intentar instalar el paquete por primera vez.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Validación de paquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2fb8fe877f68a1c787458e7703fb59f035031fc68bba1d75f24e86851aac7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074855"
---
# <a name="package-validation"></a>Validación de paquetes

Se recomienda encarecidamente que ejecute la validación en todos los paquetes de instalación nuevos o recién modificados antes de intentar instalar el paquete por primera vez.

La validación de paquetes incluye los tres procesos siguientes:

-   [Validación interna](internal-validation.md)
-   [Validación de grupo de cadenas](string-pool-validation.md)
-   [Evaluadores de coherencia internos: TIC](internal-consistency-evaluators-ices.md)

Los módulos de combinación se deben validar mediante el método descrito en [Validación de módulos de mezcla.](validating-merge-modules.md)

Evalcom2.dll proporciona un objeto COM que implementa operaciones de validación para paquetes de instalación y módulos de combinación. El objeto principal implementa interfaces para programas de C/C++. Para obtener más información, vea [Automatización de la validación.](validation-automation.md)

 

 



