---
title: Patrón de control ObjectModel
description: Describe las directrices y convenciones para implementar IObjectModelProvider, incluida la información sobre los métodos. El patrón de control ObjectModel se usa para exponer un puntero al modelo de objetos subyacente de un documento.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control ObjectModel
- Automatización de la interfaz de usuario,patrón de control ObjectModel
- Automatización de la interfaz de usuario,IObjectModelProvider
- IObjectModelProvider
- implementar el Automatización de la interfaz de usuario de control ObjectModel
- Patrón de control ObjectModel
- patrones de control,IObjectModelProvider
- patrones de control, implementar Automatización de la interfaz de usuario ObjectModel
- patrones de control, ObjectModel
- interfaces,IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62081f8fb841e7827f589fd2441c7b6411810f9a71c1c1962a0dfcf8b0e37180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114998"
---
# <a name="objectmodel-control-pattern"></a>Patrón de control ObjectModel

Describe las directrices y convenciones para implementar [**IObjectModelProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider)incluida la información sobre los métodos. El patrón de control **ObjectModel** se usa para exponer un puntero al modelo de objetos subyacente de un documento.

Muchas aplicaciones implementan modelos de objetos enriquecidos que agregan valor más allá de lo que microsoft Automatización de la interfaz de usuario proporciona. Este patrón de control permite a un cliente navegar desde un elemento Automatización de la interfaz de usuario al modelo de objetos subyacente.

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IObjectModelProvider**](#required-members-for-iobjectmodelprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **ObjectModel,** tenga en cuenta las siguientes directrices y convenciones:

-   El [**método IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) debe devolver un puntero al objeto lo más cerca posible del elemento de interfaz de usuario de origen. Por ejemplo, en un explorador web, un proveedor de Automatización de la interfaz de usuario para un único elemento debe devolver un puntero de modelo de objetos para el elemento . Devolver un puntero de modelo de objetos para la raíz del documento sería mucho menos útil.
-   Se espera que el cliente del patrón de control **ObjectModel** tenga el IID de la interfaz que buscan, por lo que es suficiente con devolver un puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) simple.
-   Dado Automatización de la interfaz de usuario serializa el puntero al proceso de cliente, el proveedor debe esperar que el cliente acceda al modelo de objetos mediante prácticas estándar del Modelo de objetos componentes (COM).

## <a name="required-members-for-iobjectmodelprovider"></a>Miembros necesarios para **IObjectModelProvider**

El método siguiente es necesario para implementar la [**interfaz IObjectModelProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider)



| Miembros requeridos                                                                             | Tipo de miembro | Notas                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | Método      | Devuelve un puntero COM al modelo de objetos subyacente. Se espera que el cliente llame al [**método IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar punteros de modelo de objetos específicos. |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 