---
description: Siga las directrices generales para aplicar los módulos de combinación descritos en aplicar módulos de combinación.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Aplicar un módulo de combinación configurable con personalizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652616"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>Aplicar un módulo de combinación configurable con personalizaciones

Siga las directrices generales para aplicar los módulos de combinación descritos en [aplicar módulos de combinación](applying-merge-modules.md). Además, los consumidores del módulo de combinación deben hacer lo siguiente para configurar un módulo de combinación en el momento de la instalación:

-   Use un módulo de combinación que se crea para tener valores configurables. Para obtener más información, consulte [crear un módulo de combinación que el usuario final pueda configurar](creating-a-merge-module-that-can-be-configured-by-the-end-user.md) .
-   Use una herramienta de combinación y configuración que llame a Mergemod.dll versión 2,0 o posterior. Las versiones anteriores de Mergmod.dll no pueden configurar los valores del módulo de fusión mediante combinación. Los autores deben crear módulos de combinación que proporcionen valores predeterminados y sean compatibles con versiones anteriores de Mergmod.dll.
-   Proporcione información de personalización cuando la herramienta de cliente de configuración la solicite. Los autores deben crear módulos de combinación que usan valores predeterminados cuando un usuario declina proporcionar información.

 

 



