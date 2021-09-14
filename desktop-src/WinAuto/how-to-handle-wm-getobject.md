---
title: Cómo controlar WM_GETOBJECT
description: Cuando recibe un mensaje GETOBJECT de WM que contiene OBJID CLIENT, el servidor debe devolver un puntero al objeto \_ \_ que implementa IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358940"
---
# <a name="how-to-handle-wm_getobject"></a>Cómo controlar WM \_ GETOBJECT

Cuando recibe un mensaje [**\_ GETOBJECT**](wm-getobject.md) de WM que contiene [**OBJID \_ CLIENT**](object-identifiers.md), el servidor debe devolver un puntero al objeto que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Este puntero es un LRESULT que se obtiene mediante una llamada [**a LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, junto con la biblioteca del modelo de objetos componentes (COM), realiza la serialización adecuada y pasa el puntero de interfaz **IAccessible** del servidor al cliente.

Los servidores deben controlar correctamente el recuento de referencias en el objeto accesible. Recuerde que cuando se crea un objeto COM, el recuento de referencias es 1. [**A continuación, LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa el recuento de referencias varias veces. Todas las referencias creadas por **LresultFromObject** se liberan automáticamente cuando el objeto ya no es necesario, pero el servidor es responsable de liberar la referencia inicial y, a menos que lo haga, el objeto nunca se destruirá. Los ejemplos de las secciones siguientes muestran cómo liberar referencias a objetos accesibles.

Normalmente, los [**servidores controlan WM \_ GETOBJECT**](wm-getobject.md) de una de las maneras siguientes:

-   [Crear nuevos objetos accesibles](create-new-accessible-objects.md)
-   [Reutilizar punteros existentes a objetos](reuse-existing-pointers-to-objects.md)
-   [Crear nuevas interfaces para el mismo objeto](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> En esta sección, como en el resto de la documentación, cuando se describe un puntero a una interfaz [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) este puntero puede ser realmente un puntero a un objeto proxy que encapsula la interfaz **IAccessible.** Para obtener más información sobre los objetos de proxy, vea [Creating Proxy Objects](creating-proxy-objects.md).

 

Para obtener información general sobre [**WM \_ GETOBJECT**](wm-getobject.md), vea [Cómo funciona WM \_ GETOBJECT](how-wm-getobject-works.md).

 

 




