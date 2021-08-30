---
description: Directrices básicas para diseñar aplicaciones COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Directrices básicas para diseñar aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d33c8000a55c85737901eb242610a0391128bbc497d485fe3bcef017d86b9f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029805"
---
# <a name="basic-guidelines-for-designing-com-applications"></a>Directrices básicas para diseñar aplicaciones COM+

Para aprovechar al máximo COM+, hay algunas directrices básicas que puede usar al crear una aplicación:

-   **Modele el estado duradero como un esquema de base de datos con la herramienta de base de datos que prefiera.** Casi todas las aplicaciones necesitan mantener un estado duradero. Las bases de datos proporcionan los servicios necesarios para crear un almacenamiento de estado duradero y escalable. Por lo tanto, el primer paso para crear una aplicación COM+ es modelar el estado duradero de la aplicación como algún tipo de esquema de base de datos. No importa realmente la base de datos que use. la mayoría de las bases de datos comerciales son compatibles con COM+. Microsoft SQL Server es un buen ejemplo de una solución que podría usar.

-   **Modele la lógica de la aplicación COM+ como un conjunto de interfaces COM.** Una vez que tenga un esquema que represente la información de estado de la aplicación, modele los intercambios que se suceden en la aplicación como interfaces COM. Estas interfaces modelarán el comportamiento de la aplicación. Esta también es la fase de desarrollo en la que debe determinar qué servicios COM+ funcionan mejor para la aplicación.

-   **Archivos DLL de componentes de compilación que contienen componentes que usan el esquema de datos físicos y exponen una vista lógica de los datos a otros componentes (el primer elemento de esta lista), así como componentes que se implementan en términos del modelo de datos lógicos (el segundo elemento de esta lista).** Una vez que tenga la estructura de la lógica y la información de estado, puede empezar a escribir código y ahora puede escribir componentes COM basados en DLL que implementan las interfaces en términos del esquema definido. Los componentes simplemente actúan como manipuladores para trabajar con la información de la base de datos y los archivos DLL de componentes permiten compilar una aplicación COM+ que funciona y que se escala correctamente.

-   **Implemente los componentes en el entorno COM+ mediante los servicios COM+ que ha seleccionado.** Una vez que haya creado la aplicación, puede implementarla en un clúster de red o de servidor. Ahora puede tomar decisiones basadas en los recursos disponibles y puede adaptar cada componente para obtener el máximo rendimiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suposiciones y principios de diseño de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Diseño de la aplicación COM+ mediante UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Diseño general Sugerencias para usar COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimización de interacciones con el nivel de lógica de negocios de COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Otras herramientas de Microsoft para compilar aplicaciones distribuidas](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



