---
title: Qué son los objetos proxy
description: Un objeto proxy actúa como intermediario entre el cliente y un objeto accesible. El propósito del objeto proxy es supervisar el intervalo de vida del objeto accesible y reenviar las llamadas al objeto accesible solo si no se destruye.
ms.assetid: fdd5d44a-1797-47e6-8044-37dde926c18a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d54fb20d677f1a417d633242ddf40c704087f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359338"
---
# <a name="what-are-proxy-objects"></a>¿Qué son los objetos proxy?

Un objeto *proxy* actúa como intermediario entre el cliente y un objeto accesible. El propósito del objeto proxy es supervisar el intervalo de vida del objeto accesible y reenviar las llamadas al objeto accesible solo si no se destruye.

Cuando un cliente llama a una propiedad [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para obtener información sobre un objeto, el objeto proxy debe comprobar si el objeto accesible sigue estando disponible. Si es así, el objeto proxy pasa la solicitud del cliente al objeto accesible. Si se destruye el objeto accesible (por ejemplo, cuando se cierra un cuadro de diálogo con controles personalizados), el objeto proxy devuelve un error. Para indicar que se ha destruido el objeto, se recomienda que los servidores devuelvan el código de error **Co \_ E \_ OBJNOTCONNECTED** porque el modelo de objetos componentes (com) devuelve este error después de que un servidor llame a [CoDisconnectObject](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject).

El objeto proxy es transparente para el cliente. Cuando el cliente llama a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), recibe un puntero a una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Sin embargo, cuando el cliente usa este puntero para llamar a cualquiera de los métodos o propiedades **IAccessible** , el código que se ejecuta se encuentra dentro del objeto proxy.

 

 