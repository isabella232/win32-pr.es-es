---
title: Introducción técnica
description: Microsoft Active Accessibility mejora el modo en que las ayuda de accesibilidad (programas especializados que ayudan a las personas con discapacidades a usar equipos de forma más eficaz) funcionan con aplicaciones que se ejecutan en Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e2bfd984dce863a2bdcdbd41d7b3d72b521861177bc4086a93eb578eb71c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325170"
---
# <a name="technical-overview"></a>Introducción técnica

Microsoft Active Accessibility mejora el modo en que las ayuda de accesibilidad (programas especializados que ayudan a las personas con discapacidades a usar equipos de forma más eficaz) funcionan con aplicaciones que se ejecutan en Microsoft Windows.

Microsoft Active Accessibility se basa en el modelo de objetos componentes (COM), desarrollado por Microsoft y es un estándar del sector que define una manera común de que las aplicaciones y los sistemas operativos se comuniquen. Microsoft Active Accessibility consta de los siguientes componentes:

-   La interfaz COM [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), que expone información sobre los elementos de la interfaz de usuario. **IAccessible** también tiene propiedades y métodos para obtener información sobre ese elemento de interfaz de usuario y manipularlo.
-   WinEvents, un sistema de eventos que permite a los servidores notificar a los clientes cuando cambia un objeto accesible.
-   Oleacc.dll, un archivo DLL de soporte técnico o en tiempo de ejecución.

El Microsoft Active Accessibility dll, Oleacc.dll, consta de los siguientes componentes:

-   Funciones que permiten a los clientes solicitar un puntero de [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (por ejemplo, [**AccessibleObjectFromWindow).**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   Funciones que permiten a los servidores devolver un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a un cliente (por ejemplo, [**LresultFromObject).**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
-   Funciones para obtener texto localizado para el rol y los códigos de estado (por ejemplo, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) y [**GetStateText).**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)
-   Algunas funciones auxiliares ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).
-   Código que proporciona la implementación predeterminada de [**IAccessible para**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) los controles USER y COMCTL estándar. Dado que implementan **IAccessible en** nombre de los controles del sistema, se conocen como *servidores proxy.*

## <a name="in-this-section"></a>En esta sección

-   [Funcionamiento de Active Accessibility](how-active-accessibility-works.md)
-   [Active Accessibility básicos](active-accessibility-basics.md)
-   [Instrucciones del servidor](server-guidelines.md)
-   [Directrices de cliente](client-guidelines.md)
-   [Instrucciones COM y Unicode](com-and-unicode-guidelines.md)

 

 




