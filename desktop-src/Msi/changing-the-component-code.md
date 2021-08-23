---
description: Al especificar los componentes para una instalación, los autores de paquetes deben seguir las reglas generales para la organización de componentes descritas en Organización de aplicaciones en componentes.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Cambiar el código de componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96217dbcdbdc63d444f95d73dec657cf1a5ddef4ed80128c85b7752e1ec0f0d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520205"
---
# <a name="changing-the-component-code"></a>Cambiar el código de componente

Al especificar los componentes [para](windows-installer-components.md) una instalación, los autores de paquetes deben seguir las reglas generales para la organización de componentes descritas en [Organización de aplicaciones en componentes](organizing-applications-into-components.md). Es posible que los autores necesiten introducir nuevos componentes o modificar los componentes existentes. Si la adición, eliminación o modificación de recursos crea eficazmente un nuevo componente, también se debe cambiar el código del componente.

## <a name="creating-a-new-component"></a>Crear un nuevo componente

Introduzca un nuevo componente y asígnele un código de componente único al realizar cualquiera de los cambios siguientes:

-   Cualquier cambio que no se haya mostrado al probar para que sea compatible con versiones anteriores del componente. En este caso, también debe cambiar el nombre o la ubicación de destino de cada recurso del componente.
-   Un cambio en el nombre o la ubicación de destino de cualquier archivo, clave del Registro, acceso directo u otro recurso del componente. En este caso, también debe cambiar el nombre o la ubicación de destino de cada recurso del componente.
-   Adición o eliminación de cualquier archivo, clave del Registro, acceso directo u otro recurso del componente. En este caso, también debe cambiar el nombre o la ubicación de destino de cada recurso del componente.
-   Volver a compilar un componente de 32 bits en un componente de 64 bits.

Al introducir un nuevo componente, los autores deben realizar una de las siguientes acciones para asegurarse de que el componente no entra en conflicto con ningún componente existente:

-   Cambie el nombre o la ubicación de destino de cualquier recurso que otro componente pueda instalar con el mismo nombre y ubicación de destino.
-   De lo contrario, se garantiza que el nuevo componente nunca se instala en la misma carpeta que otro componente que tiene un recurso bajo un nombre y una ubicación comunes. Esto incluye versiones localizadas de archivos con el mismo nombre de archivo. Para obtener más información, vea [¿Qué ocurre si se han](what-happens-if-the-component-rules-are-broken.md)roto las reglas de componente? .
-   Al cambiar el código de componente de un componente existente, cambie también el nombre o la ubicación de destino de cada archivo, clave del Registro, acceso directo y otro recurso del componente.

### <a name="creating-a-new-version-of-a-component"></a>Crear una nueva versión de un componente

A una nueva versión de un componente se le asigna el mismo código de componente que otro componente existente. Modificar un componente sin cambiar el código del componente solo es opcional en los casos siguientes:

-   Los cambios realizados en el componente se han demostrado al probar que son compatibles con versiones anteriores del componente.
-   El autor puede garantizar que la nueva versión del componente nunca se instalará en un sistema en el que entrase en conflicto con versiones anteriores del componente o aplicaciones que requieren una versión anterior. Para obtener más información, vea [¿Qué ocurre si se han](what-happens-if-the-component-rules-are-broken.md)roto las reglas de componente? .

No se debe cambiar el código de componente de una nueva versión de un componente cuando daría lugar a que dos componentes compartan recursos, como valores del Registro, archivos o accesos directos.

 

 



