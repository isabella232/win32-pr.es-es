---
title: Proxies de IAccessible
description: Los proxies IAccessible proporcionan información de accesibilidad predeterminada para los elementos de interfaz de usuario estándar, los menús de usuario y los controles comunes de COMCTL y COMCTL32.
ms.assetid: 236c2064-de44-4021-8825-f1519312dbfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dcb4cae8980e4003d9915c6783e4ddb043a8c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359154"
---
# <a name="iaccessible-proxies"></a>Proxies de IAccessible

Los proxies [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proporcionan información de accesibilidad predeterminada para los elementos de la interfaz de usuario estándar: controles de usuario, menús de usuario y controles comunes de COMCTL y comctl32. Esta compatibilidad predeterminada se expone a través de los objetos **IAccessible** creados por Oleacc.dll y ofrece soporte técnico de Microsoft Active Accessibility sin ningún trabajo de desarrollo de servidor adicional. Después, el servidor puede usar la [API de anotación dinámica](dynamic-annotation-api.md) para modificar gran parte de la información expuesta por Oleacc.dll, pero no tiene control total.

## <a name="creating-a-proxy"></a>Creación de un proxy

Para determinar si un elemento de la interfaz de usuario es compatible de forma nativa con la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , Oleacc.dll le envía un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) . Un valor devuelto distinto de cero significa que el elemento es compatible de forma nativa con Microsoft Active Accessibility y proporciona su propia compatibilidad de **IAccessible** . Sin embargo, si el valor devuelto es cero, Oleacc.dll proporciona un objeto proxy para el elemento de la interfaz de usuario e intenta devolver información significativa en su nombre. Para obtener más información acerca de **WM \_ GetObject**, consulte [how \_ GetObject Works](how-wm-getobject-works.md).

## <a name="what-information-is-exposed"></a>Qué información se expone

Oleacc.dll usa el nombre de clase de Windows del elemento de la interfaz de usuario para determinar qué información se debe exponer para cada una de sus propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y cómo recopilar esa información. Por ejemplo, Oleacc.dll llama a la función [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) para recuperar la propiedad de [**nombre**](name-property.md) de un botón de método de envío estándar, pero llama a esta misma función para recuperar la propiedad [**Value**](value-property.md) de un control de edición estándar. En efecto, Oleacc.dll asigna cada método **IAccessible** a una llamada de función o un mensaje específico de Microsoft Win32 o específico del control. Mediante el uso de esta grafía especial basada en el nombre de clase, puede devolver información significativa a través de los proxies de **IAccessible** sin ninguna compatibilidad de Microsoft Active Accessibility en el servidor.

Las aplicaciones compiladas con elementos de interfaz de usuario estándar suelen obtener soporte completo de Microsoft Active Accessibility sin ningún trabajo de desarrollo adicional. Las excepciones a esta regla son los controles de los que se han creado subclases, que no almacenan sus propias cadenas (ausencia del estilo **HASSTRINGS** ) o que están dibujadas por el propietario. En estos casos, Oleacc.dll no puede recopilar la información que necesita porque la información se almacena fuera del control. Sin embargo, en muchos de estos escenarios, soluciones alternativas o el uso de la anotación dinámica, permita que el servidor coopere con los proxies proporcionados por Oleacc.dll.

## <a name="generic-proxy-objects"></a>Objetos de proxy genéricos

Si Oleacc.dll no reconoce el nombre de clase del elemento de la interfaz de usuario, crea un proxy genérico que expone tanta información como sea posible. Como máximo, incluye el rectángulo delimitador del objeto, el objeto primario, el nombre (de la [**\_ GETTEXT de WM**](/windows/desktop/winmsg/wm-gettext)) y cualquier elemento secundario en la jerarquía de ventanas.

 

 