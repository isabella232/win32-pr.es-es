---
description: Los módulos de combinación proporcionan un método estándar mediante el cual los desarrolladores proporcionan componentes compartidos Windows Installer y la lógica de configuración a sus aplicaciones.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Combinar módulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071887"
---
# <a name="merge-modules"></a>Combinar módulos

Los módulos de combinación proporcionan un método estándar por el que los desarrolladores entregan componentes compartidos Windows [*Installer*](c-gly.md) y la lógica de configuración a sus aplicaciones. Los módulos de combinación se usan para entregar código compartido, archivos, recursos, entradas del Registro y lógica de configuración a las aplicaciones como un único archivo compuesto. Los desarrolladores que crea nuevos módulos de combinación o usan módulos de combinación existentes deben seguir el estándar descrito en esta sección.

Un módulo de combinación es similar en estructura a un archivo Windows Installer [*.msi archivo*](m-gly.md). Sin embargo, un módulo de combinación no se puede instalar por sí solo, debe combinarse en un paquete de instalación mediante una herramienta de combinación. Los desarrolladores que quieran usar módulos de combinación deben obtener una de las herramientas de combinación distribuidas libremente, como Mergemod.dll, o bien adquirir una herramienta de combinación de un proveedor de software independiente. Los desarrolladores pueden crear nuevos módulos de combinación mediante muchas de las mismas herramientas de software que se usan para crear un paquete de instalación de Windows Installer, como el editor de tablas de base de datos Orca proporcionado con el SDK del instalador de Windows.

Cuando un módulo de combinación se combina en el archivo .msi de una aplicación, toda la información y los recursos necesarios para instalar los componentes entregados por el módulo de mezcla se incorporan al archivo de .msi de la aplicación. El módulo de mezcla ya no es necesario para instalar estos componentes y el módulo de mezcla no necesita ser accesible para un usuario. Dado que toda la información necesaria para instalar los componentes se entrega como un único archivo, el uso de módulos de mezcla puede eliminar muchas instancias de conflictos de versión, entradas del Registro que faltan y archivos instalados incorrectamente.

Para obtener más información sobre los módulos de combinación, vea:

-   [Acerca de los módulos de mezcla](about-merge-modules.md)
-   [Uso de módulos de mezcla](using-merge-modules.md)
-   [Referencia del módulo de mezcla](merge-module-reference.md)

 

 



