---
description: Siga las directrices generales para aplicar módulos de mezcla descritos en Aplicar módulos de mezcla.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Aplicar un módulo de combinación configurable con personalizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159128"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>Aplicar un módulo de combinación configurable con personalizaciones

Siga las directrices generales para aplicar módulos de mezcla descritos [en Aplicar módulos de mezcla](applying-merge-modules.md). Además, los consumidores del módulo de mezcla deben hacer lo siguiente para configurar un módulo de combinación en el momento de la instalación:

-   Use un módulo de combinación que tenga una configuración configurable. Para obtener más información, vea [Creating a Merge Module that Can Be Configured by the End-User](creating-a-merge-module-that-can-be-configured-by-the-end-user.md) (Crear un módulo de mezcla que el usuario final puede configurar).
-   Use una herramienta de combinación y configuración que llame a Mergemod.dll versión 2.0 o posterior. Las versiones anteriores de Mergmod.dll no pueden configurar los valores del módulo de combinación. Los autores deben crear módulos de combinación que proporcionen valores predeterminados y sean compatibles con versiones anteriores de Mergmod.dll.
-   Proporcione información de personalización cuando se lo solicite la herramienta de cliente de configuración. Los autores deben crear módulos de combinación que usen valores predeterminados cuando un usuario rechace proporcionar información.

 

 



