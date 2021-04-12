---
title: ObjectModel (patrón de control)
description: Describe las directrices y convenciones para implementar IObjectModelProvider, incluida información sobre los métodos. El patrón de control ObjectModel se usa para exponer un puntero al modelo de objetos subyacente de un documento.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control ObjectModel
- UI Automation, ObjectModel (patrón de control)
- Automatización de la interfaz de usuario, IObjectModelProvider
- IObjectModelProvider
- implementar el patrón de control ObjectModel de automatización de la interfaz de usuario
- ObjectModel (patrón de control)
- patrones de control, IObjectModelProvider
- patrones de control, implementación de UI Automation ObjectModel
- patrones de control, ObjectModel
- interfaces, IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359189"
---
# <a name="objectmodel-control-pattern"></a>ObjectModel (patrón de control)

Describe las directrices y convenciones para implementar [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), incluida información sobre los métodos. El patrón de control **ObjectModel** se usa para exponer un puntero al modelo de objetos subyacente de un documento.

Muchas aplicaciones implementan modelos de objetos enriquecidos que agregan valor más allá de lo que proporciona automatización de la interfaz de usuario de Microsoft. Este patrón de control permite a un cliente navegar desde un elemento de automatización de la interfaz de usuario hasta el modelo de objetos subyacente.

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IObjectModelProvider**](#required-members-for-iobjectmodelprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **ObjectModel** , tenga en cuenta las siguientes directrices y convenciones:

-   El método [**IObjectModelProvider:: GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) debe devolver un puntero al objeto lo más cerca posible del elemento de la interfaz de usuario de origen. Por ejemplo, en un explorador Web, un proveedor de automatización de la interfaz de usuario para un único elemento debe devolver un puntero del modelo de objetos para el elemento. Devolver un puntero del modelo de objetos para la raíz del documento sería mucho menos útil.
-   Se espera que el cliente del patrón de control **ObjectModel** tenga el IID de la interfaz que buscan, por lo que es suficiente para devolver un puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) simple.
-   Dado que la automatización de la interfaz de usuario calcula las referencias del puntero al proceso del cliente, el proveedor debe esperar que el cliente tenga acceso al modelo de objetos mediante los procedimientos estándar del modelo de objetos componentes (COM).

## <a name="required-members-for-iobjectmodelprovider"></a>Miembros requeridos para **IObjectModelProvider**

El método siguiente es necesario para implementar la interfaz [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) .



| Miembros requeridos                                                                             | Tipo de miembro | Notas                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | Método      | Devuelve un puntero COM al modelo de objetos subyacente. Se espera que el cliente llame al método [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar punteros específicos del modelo de objetos. |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 