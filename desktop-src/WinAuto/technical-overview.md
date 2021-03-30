---
title: Introducción técnica
description: Microsoft Active Accessibility mejora la forma en que las ayudas de accesibilidad (programas especializados que ayudan a las personas con discapacidades a usar los equipos de forma más eficaz) a trabajar con aplicaciones que se ejecutan en Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778481"
---
# <a name="technical-overview"></a>Introducción técnica

Microsoft Active Accessibility mejora la forma en que las ayudas de accesibilidad (programas especializados que ayudan a las personas con discapacidades a usar los equipos de forma más eficaz) a trabajar con aplicaciones que se ejecutan en Microsoft Windows.

Microsoft Active Accessibility se basa en el modelo de objetos componentes (COM), desarrollado por Microsoft y es un estándar del sector que define una forma común para que las aplicaciones y los sistemas operativos se comuniquen. Microsoft Active Accessibility consta de los siguientes componentes:

-   La interfaz COM [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), que expone información sobre los elementos de la interfaz de usuario. **IAccessible** también tiene propiedades y métodos para obtener información sobre el elemento de interfaz de usuario y manipularlo.
-   WinEvents, un sistema de eventos que permite a los servidores notificar a los clientes el momento en que cambia un objeto accesible.
-   Oleacc.dll, un archivo DLL de soporte o de tiempo de ejecución.

El archivo DLL de Microsoft Active Accessibility, Oleacc.dll, consta de los siguientes componentes:

-   Funciones que permiten a los clientes solicitar un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (por ejemplo, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).
-   Funciones que permiten a los servidores devolver un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a un cliente (por ejemplo, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).
-   Funciones para obtener texto localizado para los códigos de rol y estado (por ejemplo, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) y [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).
-   Algunas funciones auxiliares ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).
-   Código que proporciona la implementación predeterminada de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para los controles de usuario y COMCTL estándar. Dado que estos implementan **IAccessible** en nombre de los controles del sistema, se conocen como *servidores proxy*.

## <a name="in-this-section"></a>En esta sección

-   [Cómo funciona Active Accessibility](how-active-accessibility-works.md)
-   [Aspectos básicos de Active Accessibility](active-accessibility-basics.md)
-   [Instrucciones de servidor](server-guidelines.md)
-   [Directrices de cliente](client-guidelines.md)
-   [Instrucciones COM y Unicode](com-and-unicode-guidelines.md)

 

 




