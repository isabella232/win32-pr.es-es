---
title: Exponer información adicional no cubierta por la interfaz IAccessible
description: Dependiendo de sus productos, es posible que los desarrolladores de servidores deban exponer información o funcionalidad además de Microsoft Active Accessibility compatibilidad.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba67fa0bcb11b6a87d8503d195d89b42245e680b96e98ceff96e4d05cac366f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929656"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a>Exponer información adicional no cubierta por la interfaz IAccessible

Dependiendo de sus productos, es posible que los desarrolladores de servidores deban exponer información o funcionalidad además de Microsoft Active Accessibility compatibilidad. Si este es el caso, trabaje con proveedores de tecnología de asistencia (clientes) para asegurarse de que agregan compatibilidad con las características.

No intente extender la interfaz [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Las interfaces no se pueden cambiar una vez publicadas. Para exponer información adicional, use una interfaz personalizada y exponga mediante una de las técnicas siguientes:

-   [Uso de OBJID \_ NATIVEOM para exponer una interfaz de modelo de objetos nativa para una ventana](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [Uso de QueryService para exponer una interfaz de modelo de objetos nativa para un objeto IAccessible](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

Tenga en cuenta que el objetivo de la [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es tener una interfaz bien definida que los servidores y clientes usen. Antes de exponer interfaces personalizadas, asegúrese de exponer tanta información como sea posible a través **de IAccessible**.

No se puede usar [**QueryInterface para**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) exponer interfaces personalizadas. Use **IServiceProvider::QueryService como** se describe en los procedimientos siguientes.

 

 