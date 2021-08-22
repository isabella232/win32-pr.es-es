---
description: Siga las instrucciones generales para aplicar módulos de combinación que se describen en Aplicar módulos de mezcla.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Aplicación de un módulo de combinación configurable con personalizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e9c771493a7a8e854472d840ffc21358c9741d8b3a8ea9876251456b6badf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829205"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>Aplicación de un módulo de combinación configurable con personalizaciones

Siga las instrucciones generales para aplicar módulos de combinación descritos [en Aplicar módulos de mezcla](applying-merge-modules.md). Además, los consumidores del módulo de mezcla deben hacer lo siguiente para configurar un módulo de combinación en el momento de la instalación:

-   Use un módulo de combinación que se cree para tener una configuración configurable. Para obtener más información, vea Crear un módulo de mezcla que el usuario final pueda [configurar.](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)
-   Use una herramienta de combinación y configuración que llame a Mergemod.dll versión 2.0 o posterior. Las versiones anteriores de Mergmod.dll no pueden configurar los valores del módulo de combinación. Los autores deben crear módulos de combinación que proporcionen valores predeterminados y sean compatibles con versiones anteriores de Mergmod.dll.
-   Proporcione información de personalización cuando se lo solicite la herramienta de cliente de configuración. Los autores deben crear módulos de combinación que usen valores predeterminados cuando un usuario rechace proporcionar información.

 

 



