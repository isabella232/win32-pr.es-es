---
title: Cómo controlar WM_GETOBJECT
description: Cuando recibe un mensaje de WM \_ GETOBJECT que contiene \_ el cliente de OBJID, el servidor debe devolver un puntero al objeto que implementa IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777251"
---
# <a name="how-to-handle-wm_getobject"></a>Cómo administrar WM \_ GETOBJECT

Cuando recibe un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) que contiene [**el \_ cliente de OBJID**](object-identifiers.md), el servidor debe devolver un puntero al objeto que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Este puntero es un LRESULT que se obtiene llamando a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, junto con la biblioteca del modelo de objetos componentes (COM), realiza el cálculo de referencias adecuado y pasa el puntero de interfaz **IAccessible** del servidor al cliente.

Los servidores deben controlar correctamente el recuento de referencias en el objeto accesible. Recuerde que cuando se crea un objeto COM, el recuento de referencias es 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) después incrementa el recuento de referencias varias veces. Todas las referencias creadas por **LresultFromObject** se liberan automáticamente cuando el objeto ya no se necesita, pero el servidor es responsable de liberar la referencia inicial y, a menos que lo haga, el objeto nunca se destruirá. En los ejemplos de las secciones siguientes se muestra cómo liberar referencias a objetos accesibles.

Normalmente, los servidores controlan [**WM \_ GETOBJECT**](wm-getobject.md) de una de las siguientes maneras:

-   [Crear nuevos objetos accesibles](create-new-accessible-objects.md)
-   [Reutilizar punteros existentes a objetos](reuse-existing-pointers-to-objects.md)
-   [Crear nuevas interfaces para el mismo objeto](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> En esta sección, como en el resto de la documentación, cuando se analiza un puntero a una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , este puntero puede ser realmente un puntero a un objeto proxy que contiene la interfaz **IAccessible** . Para obtener más información acerca de los objetos proxy, consulte [crear objetos proxy](creating-proxy-objects.md).

 

Para obtener información general de [**WM \_ GetObject**](wm-getobject.md), consulte [how \_ GetObject Works](how-wm-getobject-works.md).

 

 




