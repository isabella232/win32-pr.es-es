---
description: Windows Installer desarrolladores pueden crear herramientas que permitan a los usuarios finales usar módulos de combinación configurables.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Agregar capacidad de configuración de módulos a una herramienta de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813363"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a>Agregar capacidad de configuración de módulos a una herramienta de combinación

Para permitir que los usuarios finales usen módulos de combinación configurables, puede crear herramientas de combinación y configuración para hacer lo siguiente:

-   Las herramientas de combinación deben llamar a las funciones de Mergemod.dll versión 2,0 para combinar el módulo. Las versiones anteriores de Mergemod.dll no se pueden usar para configurar módulos de combinación.
-   Las aplicaciones de configuración de cliente deben interactuar con el usuario del módulo de fusión mediante combinación para recopilar las selecciones de usuario de los elementos configurables.
-   Las herramientas de combinación deben exponer la información de configuración creada en el módulo de combinación en la aplicación cliente para que el cliente pueda utilizar esta información para consultar al usuario.
-   Cuando una herramienta de combinación encuentra un elemento configurable durante una combinación, debe llamar a la herramienta de configuración de cliente para obtener información de personalización obtenida del usuario. La herramienta de combinación debe realizar los cambios especificados en el módulo de combinación.
-   Las aplicaciones de configuración deben permitir al usuario proporcionar opciones para los elementos configurables, pero no es necesario que se revelen todas las opciones posibles al usuario. La herramienta de combinación puede usar los valores predeterminados para los elementos configurables que el usuario no selecciona.
-   Si un usuario no proporciona información de personalización, las herramientas de combinación deben usar los valores de configuración predeterminados que se especifican en el módulo de combinación.
-   Después de que un usuario proporciona las selecciones específicas de la herramienta de configuración, la herramienta de combinación llama Mergemod.dll para realizar la combinación.

 

 



