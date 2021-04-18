---
title: Prácticas recomendadas para usar matrices seguras
description: Muchos métodos de interfaz de la automatización de la interfaz de usuario de Microsoft \ 32; La API toma argumentos denominados matrices seguras, del tipo de datos SAFEARRAY. En este tema se describen los procedimientos recomendados para usar matrices seguras en las aplicaciones de automatización de la interfaz de usuario.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Automatización de la interfaz de usuario, matrices seguras
- Automatización de la interfaz de usuario, proveedores
- Automatización de la interfaz de usuario, clientes
- Automatización de la interfaz de usuario, convertir entre tipos de datos
- clientes, matrices seguras
- proveedores, automatización de la interfaz de usuario
- matrices seguras
- tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704993"
---
# <a name="best-practices-for-using-safe-arrays"></a>Prácticas recomendadas para usar matrices seguras

Muchos métodos de interfaz de la API de automatización de la interfaz de usuario de Microsoft toman argumentos denominados matrices seguras, del tipo de datos [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) . En este tema se describen los procedimientos recomendados para usar matrices seguras en las aplicaciones de automatización de la interfaz de usuario.

## <a name="clients"></a>Clientes

Todas las matrices seguras que se usan con los métodos de la API de cliente de automatización de la interfaz de usuario son matrices unidimensionales de base cero. Para crear una matriz segura para un método de cliente de automatización de la interfaz de usuario, use la función [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) y para leer y escribir en una matriz segura, use las funciones [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) y [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) . Cuando termine de usar una matriz segura, destruya siempre mediante la función [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) , tanto si creó la matriz segura como si la recibió desde un método de cliente de automatización de la interfaz de usuario.

Varios métodos de automatización de la interfaz de usuario, incluidos los métodos de recuperación de propiedades como [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), recuperan [**variantes**](/windows/win32/api/oaidl/ns-oaidl-variant)s que pueden contener estructuras [**Point**](/previous-versions//dd162805(v=vs.85)) o [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) . Un **punto** se empaqueta en una **variante** como una matriz segura de dobles (VT \_ R8) con el miembro **x** en el índice 0 y el miembro **y** en el índice 1. De forma similar, un **UiaRect** se empaqueta en una **variante** como una matriz segura de valores double con los miembros **izquierdo**, **superior**, **ancho** y **alto** en los índices 0 a 3, respectivamente. En el caso de una matriz de estructuras **UiaRect** , la matriz segura contiene una matriz secuencial de cuatro valores Double para cada **UiaRect**. Los miembros **izquierdo**, **superior**, **ancho** y **alto** del primer **UiaRect** ocupan el índice 0 a 3, los miembros del segundo rectángulo ocupan el índice 4 a 7, y así sucesivamente.

La interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) incluye los siguientes métodos para la conversión entre [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) y otros tipos de datos.



| Método                                                                                               | Descripción                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation::IntNativeArrayToSafeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | Convierte una matriz de enteros en [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).                                          |
| [**IUIAutomation::IntSafeArrayToNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | Convierte un valor [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de enteros en una matriz.                                          |
| [**IUIAutomation::SafeArrayToRectNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | Convierte un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) que contiene coordenadas de rectángulo en una matriz de tipo **Rect**. |



 

## <a name="providers"></a>Proveedores

Un proveedor debe implementar una serie de métodos de interfaz que la automatización de la interfaz de usuario llama para recuperar información del proveedor. Muchas veces, esta información se compone de una matriz de valores. Para devolver una matriz a la automatización de la interfaz de usuario, el proveedor debe empaquetar la matriz en una estructura [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) . Los elementos de la matriz deben tener el tipo de datos esperado y deben aparecer en el orden esperado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Fundamentos de UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 