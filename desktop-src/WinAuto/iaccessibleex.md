---
title: La interfaz IAccessibleEx
description: Los controles que no tienen un proveedor de automatización de la interfaz de usuario de Microsoft, pero que implementan IAccessible, se pueden actualizar fácilmente para proporcionar alguna funcionalidad de automatización de la interfaz de usuario mediante la implementación de la interfaz IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148837"
---
# <a name="the-iaccessibleex-interface"></a>La interfaz IAccessibleEx

Los controles que no tienen un proveedor de automatización de la interfaz de usuario de Microsoft, pero que implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), se pueden actualizar fácilmente para proporcionar alguna funcionalidad de automatización de la interfaz de usuario mediante la implementación de la interfaz [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Esta interfaz permite que el control exponga las propiedades y los patrones de control de la automatización de la interfaz de usuario, sin necesidad de una implementación completa de las interfaces del proveedor de automatización de la interfaz de usuario, como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Para usar **IAccessibleEx**, **IRawElementProviderFragment** y todas las demás interfaces de automatización de la interfaz de usuario, incluya el archivo de encabezado UIAutomation. h en el código fuente.

Por ejemplo, considere un control personalizado que tiene un valor de intervalo. El servidor de Microsoft Active Accessibility para el control define el rol del control y puede devolver su valor actual. Sin embargo, dado que Microsoft Active Accessibility no define las propiedades mínima y máxima, el servidor carece de los medios para devolver los valores mínimo y máximo del control. Un cliente de automatización de la interfaz de usuario puede recuperar el rol del control, el valor actual y otras propiedades de Microsoft Active Accessibility, porque el núcleo de automatización de la interfaz de usuario puede obtenerlos a través de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Sin embargo, sin acceso a una interfaz [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) en el objeto, la automatización de la interfaz de usuario tampoco puede recuperar los valores máximo y mínimo.

El desarrollador del control podría proporcionar un proveedor de automatización de la interfaz de usuario completo para el control, pero esto supondría duplicar gran parte de la funcionalidad existente de la implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : por ejemplo, navegación y propiedades comunes. En su lugar, el desarrollador puede seguir confiando en **IAccessible** para proporcionar esta funcionalidad, al tiempo que agrega compatibilidad para las propiedades específicas del control a través de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

## <a name="in-this-section"></a>En esta sección

-   [Instrucciones de implementación de IAccessibleEx](iaccessibleex-implementation-guidelines.md)
-   [Implementación de IAccessibleEx para proveedores](implementing-iaccessibleex-for-providers.md)
-   [Usar IAccessibleEx desde un cliente](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Infraestructura común](common-infrastructure.md)
</dt> </dl>

 

 




