---
description: Windows Los desarrolladores del instalador pueden crear herramientas que permitan a los usuarios finales usar módulos de combinación configurables.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Agregar la funcionalidad de configuración del módulo a una herramienta de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159204"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a>Agregar la funcionalidad de configuración del módulo a una herramienta de combinación

Para permitir que los usuarios finales usen módulos de combinación configurables, puede crear herramientas de combinación y configuración para hacer lo siguiente:

-   Las herramientas de combinación deben llamar a las funciones Mergemod.dll versión 2.0 para combinar el módulo. Las versiones anteriores de Mergemod.dll no se pueden usar para configurar módulos de combinación.
-   Las aplicaciones de configuración de cliente deben interactuar con el usuario del módulo de mezcla para recopilar las selecciones de usuario para los elementos configurables.
-   Las herramientas de combinación deben exponer la información de configuración que se ha escrito en el módulo de mezcla a la aplicación cliente para que el cliente pueda usar esta información para consultar al usuario.
-   Cuando una herramienta de combinación encuentra un elemento configurable durante una combinación, debe llamar a la herramienta de configuración de cliente para obtener información de personalización obtenida del usuario. La herramienta de combinación debe realizar los cambios especificados en el módulo de combinación.
-   Las aplicaciones de configuración deben permitir que el usuario proporcione opciones para elementos configurables, pero no es necesario que todas las opciones posibles se revelan al usuario. La herramienta de combinación puede usar valores predeterminados para los elementos configurables que el usuario no selecciona.
-   Si un usuario no proporciona información de personalización, las herramientas de combinación deben usar los valores de configuración predeterminados que se especifican en el módulo de combinación.
-   Una vez que un usuario proporciona a la herramienta de configuración selecciones específicas, la herramienta de combinación llama a Mergemod.dll para realizar la combinación.

 

 



