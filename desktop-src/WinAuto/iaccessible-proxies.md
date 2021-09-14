---
title: Servidores proxy IAccessible
description: Los servidores proxy IAccessible proporcionan información de accesibilidad predeterminada para los controles USER de elementos de interfaz de usuario estándar, los menús USER y los controles comunes de COMCTL y COMCTL32.
ms.assetid: 236c2064-de44-4021-8825-f1519312dbfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dcb4cae8980e4003d9915c6783e4ddb043a8c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240920"
---
# <a name="iaccessible-proxies"></a>Servidores proxy IAccessible

Los servidores proxy [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporcionan información de accesibilidad predeterminada para los elementos de interfaz de usuario estándar: controles USER, menús USER y controles comunes de COMCTL y COMCTL32. Esta compatibilidad predeterminada se expone a través de **objetos IAccessible** creados por Oleacc.dll y ofrece compatibilidad Microsoft Active Accessibility sin trabajo adicional de desarrollo del servidor. A continuación, el servidor puede usar [la API de](dynamic-annotation-api.md) anotación dinámica para modificar gran parte de la información expuesta por Oleacc.dll, pero no tiene control completo.

## <a name="creating-a-proxy"></a>Creación de un proxy

Para determinar si un elemento de interfaz de usuario admite de forma nativa la interfaz [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Oleacc.dll envía un [**mensaje \_ GETOBJECT de WM.**](wm-getobject.md) Un valor devuelto distinto de cero significa que el elemento admite Microsoft Active Accessibility y proporciona su propia **compatibilidad con IAccessible.** Sin embargo, si el valor devuelto es cero, Oleacc.dll proporciona un objeto proxy para el elemento de interfaz de usuario e intenta devolver información significativa en su nombre. Para obtener más información sobre **WM \_ GETOBJECT**, vea [Cómo funciona WM \_ GETOBJECT](how-wm-getobject-works.md).

## <a name="what-information-is-exposed"></a>Qué información se expone

Oleacc.dll el nombre de clase Windows del elemento de interfaz de usuario para determinar qué información se debe exponer para cada una de sus [**propiedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y cómo recopilar esa información. Por ejemplo, Oleacc.dll llama a la función [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) para recuperar la propiedad [**Name**](name-property.md) de un botón de inserción estándar, pero llama a esta misma función para recuperar la propiedad [**Value**](value-property.md) de un control de edición estándar. En efecto, Oleacc.dll asigna cada método **IAccessible** a una llamada de función o mensaje específico del control adecuado de Microsoft Win32. Mediante el uso de mayúsculas y minúsculas especiales basadas en el nombre de clase, puede devolver información significativa a través de servidores proxy **IAccessible** sin Microsoft Active Accessibility compatibilidad en el servidor.

Las aplicaciones creadas con elementos de interfaz de usuario estándar normalmente obtienen compatibilidad Microsoft Active Accessibility sin trabajo de desarrollo adicional. Las excepciones a esta regla son controles que se han subclasificado, que no almacenan sus propias cadenas (ausencia del estilo **HASSTRINGS)** o que están dibujados por el propietario. En estos casos, Oleacc.dll puede recopilar la información que necesita porque la información se almacena fuera del control. Sin embargo, en muchos de estos escenarios, las soluciones alternativas establecidas o el uso de anotación dinámica permiten que el servidor colabore con los servidores proxy proporcionados por Oleacc.dll.

## <a name="generic-proxy-objects"></a>Objetos proxy genéricos

Si Oleacc.dll reconoce el nombre de clase del elemento de interfaz de usuario, crea un proxy genérico que expone tanta información como sea posible. Como máximo, esto incluye el rectángulo delimitador del objeto, el objeto primario, el nombre (de [**WM \_ GETTEXT)**](/windows/desktop/winmsg/wm-gettext)y los elementos secundarios de la jerarquía de ventanas.

 

 