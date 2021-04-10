---
description: Directrices básicas para diseñar aplicaciones COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Directrices básicas para diseñar aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153268"
---
# <a name="basic-guidelines-for-designing-com-applications"></a>Directrices básicas para diseñar aplicaciones COM+

Para sacar el máximo partido de COM+, hay algunas directrices básicas que puede usar al crear una aplicación:

-   **Modele su estado duradero como un esquema de base de datos, mediante la herramienta de base de datos que prefiera.** Casi todas las aplicaciones necesitan mantener el estado durable. Las bases de datos proporcionan los servicios necesarios para crear almacenamiento duradero y escalable del estado. Por lo tanto, el primer paso en la creación de una aplicación COM+ es modelar el estado duradero de la aplicación como algún tipo de esquema de la base de datos. En realidad, no importa qué base de datos se usa; la mayoría de las bases de datos comerciales son compatibles con COM+. Microsoft SQL Server es un buen ejemplo de una solución que puede usar.

-   **Modelar la lógica de la aplicación COM+ como un conjunto de interfaces COM.** Una vez que tenga un esquema que represente la información de estado de la aplicación, modele los intercambios que se producen en la aplicación como interfaces COM. Estas interfaces modelan el comportamiento de la aplicación. Esta es también la fase de desarrollo cuando debe determinar qué servicios COM+ funcionan mejor para su aplicación.

-   **Cree archivos dll de componentes que contengan componentes que usen el esquema de datos físico y expongan una vista lógica de los datos a otros componentes (el primer elemento de esta lista), así como los componentes que se implementan en términos del modelo de datos lógicos (el segundo elemento de esta lista).** Una vez que tenga la estructura de la información de estado y la lógica, puede empezar a escribir código y ahora puede escribir componentes COM basados en DLL que implementen las interfaces en términos del esquema definido. Los componentes simplemente actúan como manipuladores para trabajar con la información de la base de datos y los archivos dll de componentes permiten compilar una aplicación COM+ que funcione y que se escale correctamente.

-   **Implemente los componentes en el entorno COM+ mediante los servicios COM+ que ha seleccionado.** Después de compilar la aplicación, puede implementar la aplicación en un clúster de red o de servidor. Ahora puede tomar decisiones basadas en recursos disponibles y puede adaptar cada componente para obtener el máximo rendimiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Hipótesis y principios de diseño de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Diseñar la aplicación COM+ mediante UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Sugerencias de diseño generales para el uso de COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimizar interacciones con el nivel de lógica de negocios de COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Otras herramientas de Microsoft para compilar aplicaciones distribuidas](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



