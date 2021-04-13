---
description: Registro y activación de componentes en particiones
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registro y activación de componentes en particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538800"
---
# <a name="registering-and-activating-components-in-partitions"></a>Registro y activación de componentes en particiones

Después de crear una partición, el siguiente paso es registrar los componentes COM+ en esa partición. Un componente se registra en una partición cuando se crea una nueva aplicación COM+ o cuando se instala una aplicación COM+ existente en la partición. Para facilitar la administración del registro cuando varias particiones contienen los mismos componentes COM+, el servicio particiones permite a un administrador copiar aplicaciones o componentes de una partición a otra. Cuando se copia una aplicación COM+ o un componente, se copian todas las propiedades de la partición asociadas, excepto la identidad de la aplicación o cualquiera de los miembros de un rol.

Cuando el programa cliente llama a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) para crear instancias de un objeto, com+ realiza dos pasos distintos, como se indica a continuación:

1.  Busca la partición en la que reside el componente
2.  Busca el componente correcto dentro de esa partición.

En los siguientes temas de esta sección se describen estos pasos con detalle:

-   [Localizar particiones durante la activación](locating-partitions-during-activation.md)
-   [Buscar un componente para la activación](locating-a-component-for-activation.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones de diseño de aplicaciones](application-design-restrictions.md)
</dt> <dt>

[Particiones y componentes en cola de COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementación de particiones](partition-implementation.md)
</dt> <dt>

[¿Qué son las particiones COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 
