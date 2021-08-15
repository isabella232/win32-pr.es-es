---
description: Registro y activación de componentes en particiones
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registro y activación de componentes en particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf17787c953e3fe615432a8100fa71390e8aa3b8c90453a310813207ba5df7fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547067"
---
# <a name="registering-and-activating-components-in-partitions"></a>Registro y activación de componentes en particiones

Una vez creada una partición, el paso siguiente es registrar los componentes com+ dentro de esa partición. Un componente se registra dentro de una partición cuando se crea una nueva aplicación COM+ o cuando se instala una aplicación COM+ existente en la partición. Para facilitar la administración del registro cuando varias particiones contienen los mismos componentes com+, el servicio de particiones permite a un administrador copiar aplicaciones o componentes de una partición en otra. Cuando se copia una aplicación COM+ o un componente, todas las propiedades de partición asociadas se copian con ella, excepto la identidad de la aplicación o cualquiera de los miembros de un rol.

Cuando el programa cliente llama a la [**función CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) para crear una instancia de un objeto, COM+ realiza dos pasos distintos, como se muestra a continuación:

1.  Busca la partición en la que reside el componente.
2.  Busca el componente correcto dentro de esa partición.

En los temas siguientes de esta sección se describen estos pasos en detalle:

-   [Buscar particiones durante la activación](locating-partitions-during-activation.md)
-   [Buscar un componente para la activación](locating-a-component-for-activation.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones de diseño de aplicaciones](application-design-restrictions.md)
</dt> <dt>

[Componentes y particiones en cola de COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementación de particiones](partition-implementation.md)
</dt> <dt>

[¿Qué son las particiones COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 
