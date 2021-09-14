---
title: Exponer información adicional no cubierta por la interfaz IAccessible
description: En función de sus productos, es posible que los desarrolladores de servidores necesiten exponer información o funcionalidad además de Microsoft Active Accessibility compatibilidad.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160572"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a>Exponer información adicional no cubierta por la interfaz IAccessible

En función de sus productos, es posible que los desarrolladores de servidores necesiten exponer información o funcionalidad además de Microsoft Active Accessibility compatibilidad. Si este es el caso, trabaje con proveedores de tecnología de asistencia (clientes) para asegurarse de que agregan compatibilidad con las características.

No intente extender la [**interfaz IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Las interfaces no se pueden cambiar una vez publicadas. Para exponer información adicional, use una interfaz personalizada y exponga esta mediante una de las técnicas siguientes:

-   [Uso de OBJID NATIVEOM para exponer una interfaz de modelo de \_ objetos nativos para una ventana](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [Uso de QueryService para exponer una interfaz de modelo de objetos nativa para un objeto IAccessible](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

Tenga en cuenta que el objetivo de [**la interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es tener una interfaz bien definida que usen servidores y clientes. Antes de exponer interfaces personalizadas, asegúrese de exponer tanta información como sea posible a través **de IAccessible.**

No se puede [**usar QueryInterface para**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) exponer interfaces personalizadas. Use **IServiceProvider::QueryService como** se describe en los procedimientos siguientes.

 

 