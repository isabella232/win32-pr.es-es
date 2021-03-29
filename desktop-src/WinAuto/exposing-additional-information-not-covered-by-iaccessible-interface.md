---
title: Exponer información adicional no incluida en la interfaz IAccessible
description: En función de sus productos, es posible que los desarrolladores de servidores deban exponer información o funcionalidad además de la compatibilidad con Microsoft Active Accessibility.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359271"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a>Exponer información adicional no incluida en la interfaz IAccessible

En función de sus productos, es posible que los desarrolladores de servidores deban exponer información o funcionalidad además de la compatibilidad con Microsoft Active Accessibility. En este caso, trabaje con los proveedores de tecnología de asistencia (clientes) para asegurarse de que agregan compatibilidad con las características.

No intente extender la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Las interfaces no se pueden cambiar una vez que se publican. Para exponer información adicional, use una interfaz personalizada y exposición mediante una de las técnicas siguientes:

-   [Usar OBJID \_ NATIVEOM para exponer una interfaz nativa del modelo de objetos para una ventana](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [Usar QueryService para exponer una interfaz nativa del modelo de objetos para un objeto IAccessible](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

Tenga en cuenta que el objetivo de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es tener una interfaz bien definida que utilicen los servidores y los clientes. Antes de exponer las interfaces personalizadas, asegúrese de exponer tanta información como sea posible a través de **IAccessible**.

No se puede usar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para exponer interfaces personalizadas. Use **IServiceProvider:: QueryService** tal y como se describe en los procedimientos siguientes.

 

 