---
title: Procedimientos recomendados para usar Caja fuerte matrices
description: Muchos métodos de interfaz de Microsoft Automatización de la interfaz de usuario \ 32; La API toma argumentos denominados matrices seguras, del tipo de datos SAFEARRAY. En este tema se describen los procedimientos recomendados para usar matrices seguras en Automatización de la interfaz de usuario aplicaciones.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Automatización de la interfaz de usuario matrices seguras
- Automatización de la interfaz de usuario,providers
- Automatización de la interfaz de usuario,clients
- Automatización de la interfaz de usuario, conversión entre tipos de datos
- clients,safe arrays
- providers,Automatización de la interfaz de usuario
- matrices seguras
- tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ea76358f3a547b4364d01f56e850d0cbb523fc35dfbaa2870448f70c6ad5ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098125"
---
# <a name="best-practices-for-using-safe-arrays"></a>Procedimientos recomendados para usar Caja fuerte matrices

Muchos métodos de interfaz de microsoft Automatización de la interfaz de usuario API toman argumentos denominados matrices seguras, del [**tipo de datos SAFEARRAY.**](/windows/win32/api/oaidl/ns-oaidl-safearray) En este tema se describen los procedimientos recomendados para usar matrices seguras en Automatización de la interfaz de usuario aplicaciones.

## <a name="clients"></a>Clientes

Todas las matrices seguras que se usan con Automatización de la interfaz de usuario api de cliente son matrices unidimensionales de base cero. Para crear una matriz segura para un método de cliente de Automatización de la interfaz de usuario, use la función [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) y, para leer y escribir en una matriz segura, use las funciones [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) y [**SafeArrayPutElement.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) Cuando termine de usar una matriz segura, debe destruirla siempre mediante la función [**SafeArrayDestroy,**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) tanto si creó la matriz segura como si la recibió de un método Automatización de la interfaz de usuario cliente.

Varios Automatización de la interfaz de usuario, incluidos los métodos de recuperación de propiedades, [**como GetCurrentPropertyValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)recuperan [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)s que pueden contener [**estructuras POINT**](/previous-versions//dd162805(v=vs.85)) [**o UiaRect.**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) Un **point** se empaqueta en **una variant** como una matriz segura de dobles (VT R8) con el miembro x en el índice 0 y el miembro y en el índice \_ 1.   De forma similar,  un **UiaRect** se empaqueta en **una variant** como una matriz segura de dobles con los miembros izquierdos **,** **superior,** ancho y alto en los índices del 0 al 3, respectivamente. Para una matriz de **estructuras UiaRect,** la matriz segura contiene una matriz secuencial de cuatro dobles para cada **UiaRect**. Los **miembros** izquierdos ,   **superior,** ancho y alto del primer **UiaRect** ocupan el índice 0 a 3, los miembros del segundo rectángulo ocupan el índice 4 a 7, etc.

La [**interfaz IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) incluye los métodos siguientes para convertir [**entre SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) y otros tipos de datos.



| Método                                                                                               | Descripción                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation::IntNativeArrayToSafeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | Convierte una matriz de enteros en [**safearray.**](/windows/win32/api/oaidl/ns-oaidl-safearray)                                          |
| [**IUIAutomation::IntSafeArrayToNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | Convierte una [**SAFEARRAY de**](/windows/win32/api/oaidl/ns-oaidl-safearray) enteros en una matriz.                                          |
| [**IUIAutomation::SafeArrayToRectNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | Convierte una [**SAFEARRAY que**](/windows/win32/api/oaidl/ns-oaidl-safearray) contiene coordenadas de rectángulo en una matriz de tipo **RECT.** |



 

## <a name="providers"></a>Proveedores

Un proveedor debe implementar una serie de métodos de interfaz que Automatización de la interfaz de usuario llamadas para recuperar información del proveedor. Muchas veces, esta información consta de una matriz de valores. Para devolver una matriz a Automatización de la interfaz de usuario, el proveedor debe empaquetar la matriz en una [**estructura SAFEARRAY.**](/windows/win32/api/oaidl/ns-oaidl-safearray) Los elementos de la matriz deben ser del tipo de datos esperado y deben aparecer en el orden esperado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Fundamentos de UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 