---
description: Buscar un componente para la activación
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Buscar un componente para la activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51badf0b33f7c133cdea1fa95c859c2f36e282bc748c75c560d57abeead802c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306228"
---
# <a name="locating-a-component-for-activation"></a>Buscar un componente para la activación

Cuando COM+ ha ubicado la partición correcta (a través del conjunto de particiones predeterminado de la identidad del usuario, un moniker de partición o el identificador de partición en el contexto del objeto), COM+ debe buscar el componente correcto dentro de esa partición. En la ilustración siguiente se muestra cómo se encuentra y se activa un componente cuando ese componente reside en una partición.

> [!Note]  
> Antes de cualquier activación de componentes, COM+ realiza una validación para comprobar que la identidad del usuario que intenta activar el componente tiene derechos para acceder al conjunto de particiones en el que reside el componente.

 

![Diagrama que muestra un árbol de solución de problemas para buscar un componente para la activación.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

En la ilustración anterior se muestra lo siguiente:

-   Si el componente al que se llama reside en una partición y se encuentra en la misma aplicación que el componente que realiza la llamada, el componente se activa si el componente al que se llama está marcado como público o privado.
-   Si el componente al que se llama reside en una partición, pero no existe en la misma aplicación que el componente de llamada, COM+ comprueba si el componente está marcado como público. Si no se encuentra ninguna versión pública, COM+ busca en la partición global una versión pública del componente. Si no se encuentra ninguna versión pública del componente en la partición global o si la identidad del usuario no tiene derechos en la partición, se produce un error en la activación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar particiones durante la activación](locating-partitions-during-activation.md)
</dt> </dl>

 

 



