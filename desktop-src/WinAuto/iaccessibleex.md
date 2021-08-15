---
title: Interfaz IAccessibleEx
description: Los controles que no tienen un proveedor de Microsoft Automatización de la interfaz de usuario, pero que implementan IAccessible, se pueden actualizar fácilmente para proporcionar alguna funcionalidad Automatización de la interfaz de usuario mediante la implementación de la interfaz IAccessibleEx.
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170e6160a05350fa459090b2f51dbedd618ebdb81512a7e9730b50f8533ef95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566016"
---
# <a name="the-iaccessibleex-interface"></a>Interfaz IAccessibleEx

Los controles que no tienen un proveedor de Microsoft Automatización de la interfaz de usuario, pero que implementan [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)se pueden actualizar fácilmente para proporcionar alguna funcionalidad Automatización de la interfaz de usuario mediante la implementación de la [**interfaz IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) Esta interfaz permite al control exponer Automatización de la interfaz de usuario propiedades y patrones de control, sin necesidad de una implementación completa de interfaces de proveedor de Automatización de la interfaz de usuario como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment). Para usar **IAccessibleEx**, **IRawElementProviderFragment** y todas las demás interfaces Automatización de la interfaz de usuario, incluya el archivo de encabezado UIAutomation.h en el código fuente.

Por ejemplo, considere un control personalizado que tiene un valor de intervalo. El Microsoft Active Accessibility servidor del control define el rol del control y puede devolver su valor actual. Sin embargo, Microsoft Active Accessibility no define las propiedades mínima y máxima, el servidor carece de los medios para devolver los valores mínimo y máximo del control. Un Automatización de la interfaz de usuario cliente puede recuperar el rol del control, el valor actual y otras propiedades Microsoft Active Accessibility, ya que el núcleo Automatización de la interfaz de usuario puede obtenerlos a través de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Sin embargo, sin acceso a una interfaz [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) en el objeto , Automatización de la interfaz de usuario tampoco puede recuperar los valores máximo y mínimo.

El desarrollador del control podría proporcionar un proveedor de Automatización de la interfaz de usuario completo para el control, pero esto significaría duplicar gran parte de la funcionalidad existente de la implementación [**de IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) por ejemplo, la navegación y las propiedades comunes. En su lugar, el desarrollador puede seguir dependiendo de **IAccessible** para proporcionar esta funcionalidad, al tiempo que agrega compatibilidad con propiedades específicas del control a través [**de IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).

## <a name="in-this-section"></a>En esta sección

-   [Instrucciones de implementación de IAccessibleEx](iaccessibleex-implementation-guidelines.md)
-   [Implementación de IAccessibleEx para proveedores](implementing-iaccessibleex-for-providers.md)
-   [Uso de IAccessibleEx desde un cliente](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Infraestructura común](common-infrastructure.md)
</dt> </dl>

 

 




