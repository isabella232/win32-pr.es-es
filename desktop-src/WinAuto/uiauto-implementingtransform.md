---
title: Transformar patrón de control
description: Describe directrices y convenciones para implementar ITransformProvider e ITransformProvider2, incluida información sobre propiedades y métodos.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Transformar
- Automatización de la interfaz de usuario,Transformar patrón de control
- Automatización de la interfaz de usuario,ITransformProvider
- ITransformProvider
- implementación de Automatización de la interfaz de usuario de control transformar
- Transformación de patrones de control
- patrones de control,ITransformProvider
- patrones de control, implementar Automatización de la interfaz de usuario transformación
- patrones de control,Transformar
- interfaces,ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465996"
---
# <a name="transform-control-pattern"></a>Transformar patrón de control

Describe directrices y convenciones para implementar [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) e [**ITransformProvider2,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2)incluida información sobre propiedades y métodos. El patrón de control Transformar se usa para admitir controles que se pueden mover, cambiar de tamaño o girar dentro de un espacio bidimensional.

Para obtener ejemplos de controles que implementan este patrón de control, vea [Tipos de control y sus patrones de control admitidos.](uiauto-controlpatternmapping.md)

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **ITransformProvider**](#required-members-for-itransformprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **Transformar,** tenga en cuenta las siguientes directrices y convenciones:

-   La compatibilidad con este patrón de control no se limita a los objetos del escritorio. Este patrón de control también lo admite los elementos secundarios de un objeto contenedor si los elementos secundarios se pueden mover, cambiar de tamaño o girar libremente dentro de los límites del contenedor.
-   Un objeto no se puede mover, cambiar de tamaño o girar de manera que su ubicación en pantalla resultante quede completamente fuera de las coordenadas de su contenedor y que, por tanto, sea inaccesible para el teclado o el mouse (por ejemplo, cuando una ventana de nivel superior se mueva fuera de la pantalla o un objeto secundario se mueva fuera de los límites de la ventanilla del contenedor). En estos casos, el objeto se coloca lo más cerca posible de las coordenadas de pantalla solicitadas reemplazando las coordenadas superiores o izquierdas para que se encuentren dentro de los límites del contenedor.
-   Para sistemas de varios monitores, si se mueve un objeto, cambia de tamaño o gira completamente fuera de las coordenadas de pantalla de escritorio combinadas, el objeto se coloca en el monitor principal lo más cerca posible de las coordenadas solicitadas.
-   Todos los parámetros y los valores de propiedad son absolutos e independientes de la configuración regional.

## <a name="required-members-for-itransformprovider"></a>Miembros necesarios para **ITransformProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz ITransformProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)



| Miembros requeridos                                         | Tipo de miembro | Notas |
|----------------------------------------------------------|-------------|-------|
| [**CanMove**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | Propiedad    | None  |
| [**CanResize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | Propiedad    | None  |
| [**CanRotate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | Propiedad    | None  |
| [**Mover**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | Método      | None  |
| [**Cambiar de tamaño**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | Método      | None  |
| [**Girar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | Método      | None  |



 

Las siguientes propiedades y métodos adicionales son necesarios para implementar la [**interfaz ITransformProvider2.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)



| Miembros requeridos                                              | Tipo de miembro | Notas |
|---------------------------------------------------------------|-------------|-------|
| [**CanZoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | Propiedad    | None  |
| [**Zoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | Método      | None  |
| [**ZoomByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | Método      | None  |
| [**ZoomLevel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | Propiedad    | None  |
| [**ZoomMaximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | Propiedad    | None  |
| [**ZoomMinimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | Propiedad    | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 