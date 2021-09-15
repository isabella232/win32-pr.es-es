---
description: Al desarrollar aplicaciones COM+, las tareas principales incluyen el diseño de componentes COM para encapsular la lógica de la aplicación y la integración de estos componentes en una aplicación COM+, la creación de la aplicación COM+ y la administración de la aplicación a través de la implementación y el mantenimiento.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Desarrollo de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465692"
---
# <a name="developing-com-applications"></a>Desarrollo de aplicaciones COM+

Al desarrollar aplicaciones COM+, las tareas principales incluyen el diseño de componentes COM para encapsular la lógica de la aplicación y la integración de estos componentes en una aplicación COM+, la creación de la aplicación COM+ y la administración de la aplicación a través de la implementación y el mantenimiento.

## <a name="designing-com-components"></a>Diseño de componentes COM

En los pasos siguientes se describe un procedimiento general para un buen diseño de componentes:

1.  Defina las clases COM y las clases de implementación.
2.  Agrupa las clases en componentes.
3.  Seleccione el conjunto de servicios COM+ para el componente, incluso si no especifica todos ellos al desarrollar el componente. Estos servicios se pueden especificar más adelante mediante la herramienta administrativa Servicios de componentes o el modelo de objetos de administración de COM+ (consulte Automatización de la administración de [COM+](automating-com--administration.md) para obtener más información sobre el modelo de objetos de administración de COM+).

## <a name="creating-the-com-application"></a>Creación de la aplicación COM+

Después de diseñar los componentes COM, el desarrollador integra los componentes en una aplicación COM+ y configura la aplicación. Los siguientes pasos describen el proceso:

1.  Integre los componentes en una aplicación COM+. Puede integrar los componentes en una aplicación COM+ existente o crear una nueva aplicación (vacía) para los componentes. (Consulte [Creación de aplicaciones COM+).](creating-com--applications.md)
2.  Especifique el conjunto correcto de atributos para cada una de las clases (si las hay, y si no se especifican en la herramienta de desarrollo). Estos atributos expresan las dependencias de componentes en cualquier servicio COM+ en el que su implementación pueda basarse (por ejemplo, transacciones, componentes en cola, seguridad, agrupación de objetos y activación Just-In-Time).
3.  Configure el marco de seguridad (roles y asignación de roles a clases, interfaces y métodos).
4.  Configure atributos específicos del entorno en clases y aplicaciones (por ejemplo, el tamaño predeterminado del grupo de objetos). El administrador del sistema puede establecer (o modificar posteriormente) estos atributos específicos del entorno.
5.  Exporte la aplicación para su redistribución e implementación.

Para obtener información más detallada sobre los pasos para diseñar aplicaciones distribuidas, vea [Diseño de aplicaciones COM+.](designing-com--applications.md)

## <a name="administering-com-applications"></a>Administración de aplicaciones COM+

Normalmente, un desarrollador entrega una aplicación COM+ configurada parcialmente al administrador del sistema. A continuación, el administrador puede personalizar la aplicación para uno o varios entornos específicos (por ejemplo, agregando cuentas de usuario en roles y nombres de servidor en un clúster de aplicaciones). Entre las tareas del administrador se incluyen las siguientes:

-   Instalación de la aplicación COM+ configurada parcialmente en un equipo administrativo.
-   Proporcionar atributos específicos del entorno, como miembros de rol y tamaño del grupo de objetos.
-   Volver a exportar la aplicación COM+ totalmente configurada.
-   Creación de un proxy de aplicación (si se va a acceder a la aplicación de forma remota).

Una vez que una aplicación está completamente configurada para un entorno específico, el administrador puede implementarla en máquinas de prueba o producción. Esto implica la instalación de la aplicación COM+ totalmente configurada en uno o varios equipos.

Para obtener información detallada sobre los procedimientos de administración de COM+, consulte la herramienta administrativa Servicios de componentes.

 

 



