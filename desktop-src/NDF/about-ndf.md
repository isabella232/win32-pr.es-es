---
title: Acerca de NDF
description: El marco de diagnóstico de redes (NDF) reduce la implicación de los administradores de red y los usuarios de equipos al controlar los problemas de red más comunes a medida que se producen.
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b638298fe321d314815c74fced49d3dfb623022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775325"
---
# <a name="about-ndf"></a>Acerca de NDF

El marco de diagnóstico de redes (NDF) reduce la implicación de los administradores de red y los usuarios de equipos al controlar los problemas de red más comunes a medida que se producen. Mediante el uso de las funcionalidades de diagnóstico y reparación de NDF, los usuarios y los administradores no necesitan herramientas adicionales para controlar algunos problemas relativamente comunes. NDF se incluye como parte de Windows Vista, Windows Server 2008 y versiones posteriores. Está disponible siempre que se arranca un sistema (pero no se puede ejecutar en modo seguro).

## <a name="ndf-helper-classes"></a>Clases auxiliares de NDF

NDF incluye clases auxiliares que diagnostican problemas de red a medida que se producen. Cada una de estas clases auxiliares contiene la lógica necesaria para solucionar problemas de al menos un componente o aplicación.

Las clases auxiliares de NDF individuales realizan las tareas principales de la sesión de diagnóstico. Cada clase auxiliar es una unidad de código diseñada para evaluar un aspecto de estado de su componente de red respectivo. La clase auxiliar también entiende qué opciones de reparación posibles están disponibles para restaurar el estado del componente, así como el costo y el riesgo de cualquier opción de reparación determinada.

Cada clase auxiliar se conecta al marco general de diagnósticos de red. Si un componente de red de terceros incluye una clase auxiliar de NDF, otras aplicaciones pueden resolver los problemas con ese componente, sin necesidad de tener conocimientos específicos de ese componente.

Las clases auxiliares desarrolladas por Microsoft proporcionan a los desarrolladores de software la funcionalidad principal de diagnóstico y reparación. También hay un pequeño conjunto de API que los desarrolladores pueden usar para diagnosticar problemas de red mediante NDF. Para obtener más información, vea ejemplo de [funciones NDF](ndf-functions.md) y [diagnósticos NDF](ndf-diagnostics-example.md).

## <a name="extensible-helper-classes"></a>Clases auxiliares extensibles

En algunos casos, los desarrolladores de aplicaciones pueden proporcionar una funcionalidad más específica de diagnóstico y reparación.

Algunas de las clases auxiliares de NDF de Microsoft están diseñadas para ampliarse con el fin de proporcionar funcionalidades adicionales de diagnóstico y reparación. Esto significa que los desarrolladores pueden incluir funcionalidad para usar las funcionalidades de diagnóstico y reparación de NDF para solucionar problemas específicos de su software o hardware.

Por ejemplo, el equipo inalámbrico de Microsoft proporciona una clase auxiliar extensible que permite a los proveedores inalámbricos de terceros agregar lógica de solución de problemas específica para su hardware o software específico. Para ello, se puede desarrollar una extensión de clase auxiliar NDF. Para obtener más información, consulte [las clases auxiliares extensibles de diagnóstico inalámbrico de 802,11](802-11-wireless-diagnostics-extensible-helper-classes.md).

Una extensión de clase auxiliar NDF, por definición, extiende la funcionalidad de una clase auxiliar extensible existente. Si una clase auxiliar no es extensible, nadie puede escribir una extensión para esa clase auxiliar.

## <a name="benefits-of-helper-class-extensions"></a>Ventajas de las extensiones de clase auxiliares

NDF ofrece varias ventajas distintivas para alentar su uso por parte de los desarrolladores de componentes de red. En la parte superior de la lista, los clientes del software del proveedor liberarán algunos de sus propios recursos de solución de problemas y reducirán el costo total de propiedad. Una extensión de clase auxiliar bien escrita también proporciona las siguientes ventajas:

-   Permite a un equipo determinar si su componente no es la causa de un problema de conectividad. Por ejemplo, las redes se suelen culpar por problemas de conectividad que no son realmente el resultado de un error del componente de red. Al escribir una extensión de clase auxiliar, un equipo puede descartar más fácilmente un componente determinado como causa de un error de conectividad.
-   Permite a un equipo diagnosticar y depurar rápidamente un problema en el componente. Se puede eliminar el tiempo dedicado a la depuración y la solución de problemas si se escribe una clase auxiliar para realizar todos los pasos de diagnóstico estándar que se necesitarían de todos modos.
-   Elimina la necesidad de escribir y admitir herramientas de uso único para diagnosticar problemas. Una clase auxiliar puede ser el repositorio central de las capacidades de diagnóstico de un componente y las técnicas de recopilación de información.
-   Hace que los diagnósticos específicos del componente estén disponibles para las aplicaciones, sin necesidad de tener conocimiento directo del componente.

 

 




