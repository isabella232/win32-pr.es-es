---
title: Cómo controlar WM_GETOBJECT
description: Cuando recibe un mensaje WM GETOBJECT que contiene OBJID CLIENT, el servidor debe devolver un puntero al objeto que \_ \_ implementa IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f066ee42ffaeee2d585ac5480e5af31acf14c87ba9994d3d338b65e6cf427a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052733"
---
# <a name="how-to-handle-wm_getobject"></a>Cómo controlar WM \_ GETOBJECT

Cuando recibe un mensaje [**\_ WM GETOBJECT**](wm-getobject.md) que contiene [**OBJID \_ CLIENT**](object-identifiers.md), el servidor debe devolver un puntero al objeto que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Este puntero es un LRESULT que se obtiene mediante una llamada [**a LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, junto con la biblioteca del Modelo de objetos componentes (COM), realiza la serialización adecuada y pasa el puntero de interfaz **IAccessible** del servidor al cliente.

Los servidores deben controlar correctamente el recuento de referencias en el objeto accesible. Recuerde que cuando se crea un objeto COM, el recuento de referencias es 1. [**A continuación, LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa el recuento de referencias varias veces. Todas las referencias creadas por **LresultFromObject** se liberan automáticamente cuando el objeto ya no es necesario, pero el servidor es responsable de liberar la referencia inicial y, a menos que lo haga, el objeto nunca se destruirá. En los ejemplos de las secciones siguientes se muestra cómo liberar referencias a objetos accesibles.

Normalmente, los [**servidores \_ controlan WM GETOBJECT**](wm-getobject.md) de una de las maneras siguientes:

-   [Crear nuevos objetos accesibles](create-new-accessible-objects.md)
-   [Reutilizar punteros existentes a objetos](reuse-existing-pointers-to-objects.md)
-   [Crear nuevas interfaces para el mismo objeto](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> En esta sección como en el resto de la documentación, cuando se describe un puntero a una interfaz [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) este puntero puede ser realmente un puntero a un objeto proxy que encapsula la **interfaz IAccessible.** Para obtener más información sobre los objetos de proxy, vea [Creating Proxy Objects](creating-proxy-objects.md).

 

Para obtener información general sobre [**WM \_ GETOBJECT**](wm-getobject.md), vea [Funcionamiento de WM \_ GETOBJECT.](how-wm-getobject-works.md)

 

 




