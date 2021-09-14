---
description: Al especificar los componentes para una instalación, los autores de paquetes deben seguir las reglas generales para la organización de componentes descritas en Organización de aplicaciones en componentes.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Cambiar el código del componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7531b4a38312d4abed038b612c4292c44af8e967
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158932"
---
# <a name="changing-the-component-code"></a>Cambiar el código del componente

Al especificar los componentes [para una](windows-installer-components.md) instalación, los autores de paquetes deben seguir las reglas generales para la organización de componentes descritas en Organización de aplicaciones [en componentes](organizing-applications-into-components.md). Es posible que los autores necesiten introducir nuevos componentes o modificar los componentes existentes. Si la adición, eliminación o modificación de recursos crea eficazmente un nuevo componente, también se debe cambiar el código del componente.

## <a name="creating-a-new-component"></a>Crear un nuevo componente

Introduzca un nuevo componente y asígnele un código de componente único al realizar cualquiera de los cambios siguientes:

-   Cualquier cambio que no se haya mostrado al probar para que sea compatible con versiones anteriores del componente. En este caso, también debe cambiar el nombre o la ubicación de destino de cada recurso del componente.
-   Un cambio en el nombre o la ubicación de destino de cualquier archivo, clave del Registro, acceso directo u otro recurso del componente. En este caso, también debe cambiar el nombre o la ubicación de destino de cada recurso del componente.
-   La adición o eliminación de cualquier archivo, clave del Registro, acceso directo u otro recurso del componente. En este caso, también debe cambiar el nombre o la ubicación de destino de cada recurso del componente.
-   Volver a compilar un componente de 32 bits en un componente de 64 bits.

Al introducir un nuevo componente, los autores deben realizar una de las siguientes acciones para asegurarse de que el componente no entre en conflicto con los componentes existentes:

-   Cambie el nombre o la ubicación de destino de cualquier recurso que otro componente pueda instalar con el mismo nombre y ubicación de destino.
-   De lo contrario, se garantiza que el nuevo componente nunca se instala en la misma carpeta que otro componente que tiene un recurso con un nombre y una ubicación comunes. Esto incluye versiones localizadas de archivos con el mismo nombre de archivo. Para obtener más información, vea [¿Qué ocurre si se han](what-happens-if-the-component-rules-are-broken.md)roto las reglas de componentes? .
-   Al cambiar el código de componente de un componente existente, cambie también el nombre o la ubicación de destino de cada archivo, clave del Registro, acceso directo y otro recurso del componente.

### <a name="creating-a-new-version-of-a-component"></a>Crear una nueva versión de un componente

A una nueva versión de un componente se le asigna el mismo código de componente que otro componente existente. La modificación de un componente sin cambiar el código del componente solo es opcional en los casos siguientes:

-   Se ha demostrado que los cambios realizados en el componente son compatibles con todas las versiones anteriores del componente.
-   El autor puede garantizar que la nueva versión del componente nunca se instalará en un sistema en el que entre en conflicto con las versiones anteriores del componente o las aplicaciones que requieren una versión anterior. Para obtener más información, vea [¿Qué ocurre si se han](what-happens-if-the-component-rules-are-broken.md)roto las reglas de componentes? .

El código de componente de una nueva versión de un componente no debe cambiarse cuando daría lugar a que dos componentes compartan recursos, como valores del Registro, archivos o accesos directos.

 

 



