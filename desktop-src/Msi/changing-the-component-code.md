---
description: Al especificar los componentes para una instalación, los autores de paquetes deben seguir las reglas generales de la organización de componentes descrita en organización de aplicaciones en componentes.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Cambiar el código del componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7531b4a38312d4abed038b612c4292c44af8e967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667004"
---
# <a name="changing-the-component-code"></a>Cambiar el código del componente

Al especificar los [componentes](windows-installer-components.md) para una instalación, los autores de paquetes deben seguir las reglas generales de la organización de componentes descrita en organización de [aplicaciones en componentes](organizing-applications-into-components.md). Es posible que los autores deban introducir nuevos componentes o modificar los existentes. Si la adición, eliminación o modificación de recursos crea eficazmente un componente nuevo, el código del componente también debe cambiarse.

## <a name="creating-a-new-component"></a>Crear un nuevo componente

Introduzca un componente nuevo y asígnele un código de componente único cuando realice cualquiera de los siguientes cambios:

-   Cualquier cambio que no se haya mostrado probando para ser compatible con versiones anteriores del componente. En este caso, también debe cambiar el nombre o la ubicación de destino de cada recurso del componente.
-   Un cambio en el nombre o la ubicación de destino de cualquier archivo, clave del registro, acceso directo u otro recurso del componente. En este caso, también debe cambiar el nombre o la ubicación de destino de cada recurso del componente.
-   Adición o eliminación de cualquier archivo, clave del registro, acceso directo u otro recurso del componente. En este caso, también debe cambiar el nombre o la ubicación de destino de cada recurso del componente.
-   Volver a compilar un componente de 32 bits en un componente de 64 bits.

Al introducir un nuevo componente, los autores deben realizar una de las siguientes acciones para asegurarse de que el componente no entra en conflicto con ningún componente existente:

-   Cambiar el nombre o la ubicación de destino de cualquier recurso que otro componente pueda instalar en el mismo nombre y ubicación de destino.
-   De lo contrario, asegúrese de que el nuevo componente nunca se instala en la misma carpeta que otro componente que tiene un recurso bajo un nombre y una ubicación comunes. Esto incluye las versiones localizadas de los archivos con el mismo nombre de archivo. Para obtener más información, consulte [¿Qué ocurre si se interrumpen las reglas de componentes?](what-happens-if-the-component-rules-are-broken.md)
-   Al cambiar el código de componente de un componente existente, cambie también el nombre o la ubicación de destino de todos los archivos, claves del registro, accesos directos y otros recursos del componente.

### <a name="creating-a-new-version-of-a-component"></a>Crear una nueva versión de un componente

A una nueva versión de un componente se le asigna el mismo código de componente que otro componente existente. Modificar un componente sin cambiar el código de componente solo es opcional en los casos siguientes:

-   Los cambios en el componente se han demostrado probando para ser compatibles con todas las versiones anteriores del componente.
-   El autor puede garantizar que la nueva versión del componente nunca se instalará en un sistema en el que pueda entrar en conflicto con las versiones anteriores del componente o las aplicaciones que requieren una versión anterior. Para obtener más información, consulte [¿Qué ocurre si se interrumpen las reglas de componentes?](what-happens-if-the-component-rules-are-broken.md)

No se debe cambiar el código de componente de una nueva versión de un componente cuando se haría con dos componentes que comparten recursos, como valores del registro, archivos o accesos directos.

 

 



