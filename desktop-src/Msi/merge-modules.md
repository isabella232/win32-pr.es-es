---
description: Los módulos de combinación proporcionan un método estándar por el que los desarrolladores ofrecen componentes compartidos de Windows Installer y lógica de configuración a sus aplicaciones.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279150"
---
# <a name="merge-modules"></a>Módulos de combinación

Los módulos de combinación proporcionan un método estándar por el que los desarrolladores ofrecen [*componentes*](c-gly.md) compartidos de Windows Installer y lógica de configuración a sus aplicaciones. Los módulos de combinación se utilizan para proporcionar código compartido, archivos, recursos, entradas del registro y lógica de instalación a las aplicaciones como un solo archivo compuesto. Los desarrolladores que crean nuevos módulos de combinación o utilizan módulos de combinación existentes deben seguir el estándar descrito en esta sección.

Un módulo de combinación tiene una estructura similar a la de un [*archivo Windows Installer. msi*](m-gly.md)simplificado. Sin embargo, un módulo de combinación no se puede instalar por sí solo, debe combinarse en un paquete de instalación mediante una herramienta de combinación. Los desarrolladores que deseen utilizar módulos de combinación deben obtener una de las herramientas de combinación distribuida libremente, como Mergemod.dll, o adquirir una herramienta de fusión mediante combinación de un fabricante de software independiente. Los desarrolladores pueden crear módulos de fusión mediante combinación con muchas de las herramientas de software que se usan para crear un paquete de instalación de Windows Installer, como el editor de tablas de base de datos Orca proporcionado con el SDK de Windows Installer.

Cuando se combina un módulo de combinación en el archivo. msi de una aplicación, toda la información y los recursos necesarios para instalar los componentes proporcionados por el módulo de combinación se incorporan en el archivo. msi de la aplicación. El módulo de combinación ya no es necesario para instalar estos componentes y no es necesario que el módulo de combinación sea accesible para un usuario. Dado que toda la información necesaria para instalar los componentes se entrega como un solo archivo, el uso de módulos de combinación puede eliminar muchas instancias de conflictos de versiones, entradas del registro que faltan y archivos que no se instalan correctamente.

Para obtener más información acerca de los módulos de combinación, vea:

-   [Acerca de los módulos de combinación](about-merge-modules.md)
-   [Usar módulos de combinación](using-merge-modules.md)
-   [Referencia del módulo de combinación](merge-module-reference.md)

 

 



