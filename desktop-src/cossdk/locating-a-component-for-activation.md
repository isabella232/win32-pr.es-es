---
description: Buscar un componente para la activación
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Buscar un componente para la activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104552398"
---
# <a name="locating-a-component-for-activation"></a>Buscar un componente para la activación

Cuando COM+ encuentra la partición correcta, a través del conjunto de particiones predeterminado de la identidad del usuario, un moniker de la partición o el identificador de la partición en el contexto del objeto, COM + debe localizar el componente correcto dentro de esa partición. En la ilustración siguiente se muestra cómo se encuentra y se activa un componente cuando ese componente reside en una partición.

> [!Note]  
> Antes de cualquier activación de componentes, COM+ realiza una validación para comprobar que la identidad de usuario que intenta activar el componente tiene derechos de acceso al conjunto de particiones en el que reside el componente.

 

![Diagrama que muestra un árbol de solución de problemas para buscar un componente para la activación.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

En la ilustración anterior se muestra lo siguiente:

-   Si el componente que se está llamando reside en una partición y está en la misma aplicación que el componente que realiza la llamada, el componente se activa si el componente al que se llama está marcado como público o privado.
-   Si el componente al que se llama reside en una partición, pero no existe en la misma aplicación que el componente que realiza la llamada, COM+ comprueba para ver si el componente está marcado como público. Si no se encuentra ninguna versión pública, COM+ busca en la partición global para encontrar una versión pública del componente. Si no se encuentra ninguna versión pública del componente en la partición global o si la identidad del usuario no tiene derechos en la partición, se produce un error en la activación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Localizar particiones durante la activación](locating-partitions-during-activation.md)
</dt> </dl>

 

 



