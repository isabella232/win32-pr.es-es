---
title: Acerca de NDF
description: El Marco de diagnóstico de redes (NDF) reduce la participación de los administradores de red y los usuarios del equipo al controlar los problemas comunes de red a medida que se producen.
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2ce4890645e83c27e9c1cf594d7fbf4d81ce3d662a2b470ce652c71e7d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798907"
---
# <a name="about-ndf"></a>Acerca de NDF

El Marco de diagnóstico de redes (NDF) reduce la participación de los administradores de red y los usuarios del equipo al controlar los problemas comunes de red a medida que se producen. Al usar las funcionalidades de diagnóstico y reparación de NDF, los usuarios y administradores no necesitan herramientas adicionales para controlar algunos problemas relativamente comunes. NDF se distribuye como parte de Windows Vista, Windows Server 2008 y versiones posteriores. Está disponible cada vez que se arranca un sistema (pero no se puede ejecutar en Caja fuerte automático).

## <a name="ndf-helper-classes"></a>Clases auxiliares de NDF

NDF incluye clases auxiliares que diagnostican problemas de red a medida que se producen. Cada una de estas clases auxiliares contiene la lógica necesaria para solucionar problemas de al menos un componente o aplicación.

Las clases auxiliares de NDF individuales realizan las tareas principales de la sesión de diagnóstico. Cada clase auxiliar es una unidad de código diseñada para evaluar un aspecto de mantenimiento de su respectivo componente de red. La clase auxiliar también entiende qué posibles opciones de reparación están disponibles para restaurar el estado del componente, así como el costo y el riesgo de cualquier opción de reparación determinada.

Cada clase auxiliar se conecta al conjunto Marco de diagnóstico de redes. Si un componente de red de terceros incluye una clase auxiliar NDF, otras aplicaciones que usan NDF pueden resolver los problemas con ese componente, sin necesidad de que tengan conocimientos específicos de ese componente.

Las clases auxiliares desarrolladas por Microsoft proporcionan a los desarrolladores de software la funcionalidad principal de diagnóstico y reparación. También hay un pequeño conjunto de API que los desarrolladores pueden usar para diagnosticar problemas de red mediante NDF. Para obtener más información, vea [Funciones de NDF y](ndf-functions.md) Ejemplo de diagnóstico de [NDF](ndf-diagnostics-example.md).

## <a name="extensible-helper-classes"></a>Clases auxiliares extensibles

En algunos casos, los desarrolladores de aplicaciones pueden proporcionar funcionalidades de diagnóstico y reparación más específicas.

Algunas de las clases auxiliares de NDF de Microsoft están diseñadas para ampliarse para proporcionar funcionalidades adicionales de diagnóstico y reparación. Esto significa que los desarrolladores pueden incluir funcionalidades para usar funcionalidades de diagnóstico y reparación de NDF para solucionar problemas específicos de su software o hardware.

Por ejemplo, el equipo inalámbrico de Microsoft proporciona una clase auxiliar extensible que permite a cualquier proveedor inalámbrico de terceros agregar lógica de solución de problemas específica para su hardware o software específico. Para ello, pueden desarrollar una extensión de clase auxiliar de NDF. Para obtener más información, vea [802.11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md).

Una extensión de clase auxiliar de NDF, por definición, amplía la funcionalidad de una clase auxiliar extensible existente. Si una clase auxiliar no es extensible, nadie puede escribir una extensión para esa clase auxiliar.

## <a name="benefits-of-helper-class-extensions"></a>Ventajas de las extensiones de clase auxiliar

NDF ofrece varias ventajas distintas para fomentar su uso por parte de los desarrolladores de componentes de red. En la parte superior de la lista, los clientes del software del proveedor liberarán algunos de sus propios recursos de solución de problemas y reducirán el costo total de propiedad. Una extensión de clase auxiliar bien escrita también proporciona las siguientes ventajas:

-   Permite a un equipo determinar cuándo su componente no es la causa de un problema de conectividad. Por ejemplo, a menudo se culpa a las redes de problemas de conectividad que no son realmente el resultado de un error del componente de red. Al escribir una extensión de clase auxiliar, un equipo puede descartar más fácilmente un componente determinado como la causa de un error de conectividad.
-   Permite a un equipo diagnosticar y depurar rápidamente un problema dentro del componente. El tiempo dedicado a la depuración y la solución de problemas se puede eliminar si se escribe una clase auxiliar para realizar todos los pasos de diagnóstico estándar que serían necesarios de todos modos.
-   Elimina la necesidad de escribir y admitir herramientas únicas para diagnosticar problemas. Una clase auxiliar puede ser el repositorio central de las funcionalidades de diagnóstico y las técnicas de recopilación de información de un componente.
-   Hace que los diagnósticos específicos del componente estén disponibles para las aplicaciones, sin necesidad de que tengan ningún conocimiento directo sobre el componente.

 

 




