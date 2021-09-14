---
title: Patrón de control MultipleView
description: Describe directrices y convenciones para implementar IMultipleViewProvider, incluida información sobre propiedades y métodos.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Automatización de la interfaz de usuario, implementación del patrón de control MultipleView
- Automatización de la interfaz de usuario,patrón de control MultipleView
- Automatización de la interfaz de usuario,IMultipleViewProvider
- IMultipleViewProvider
- implementación de Automatización de la interfaz de usuario de control MultipleView
- Patrones de control MultipleView
- patrones de control,IMultipleViewProvider
- patrones de control, implementar Automatización de la interfaz de usuario MultipleView
- patrones de control,MultipleView
- interfaces,IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070490"
---
# <a name="multipleview-control-pattern"></a>Patrón de control MultipleView

Describe directrices y convenciones para implementar [**IMultipleViewProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)incluida información sobre propiedades y métodos. Al final del tema se ofrecen vínculos a referencias adicionales. El patrón de control **MultipleView** se usa para admitir controles que proporcionan y pueden cambiar entre varias representaciones de la misma información o del mismo conjunto de controles secundarios.

Entre los ejemplos de controles que pueden presentar varias vistas se incluyen la vista de lista (que puede mostrar su contenido como miniaturas, iconos, iconos o detalles), gráficos de Microsoft Excel (circular, línea, barra, valor de celda con una fórmula), documentos de Microsoft Word (normal, diseño web, diseño de impresión, diseño de lectura, esquema), calendario de Microsoft Outlook (año, mes, semana, día) y máscaras de Microsoft Reproductor de Windows Media. Las vistas admitidas las determina el desarrollador del control y son específicas de cada control.

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros necesarios para **IMultipleViewProvider**](#required-members-for-imultipleviewprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **MultipleView,** tenga en cuenta las siguientes directrices y convenciones:

-   [**IMultipleViewProvider también**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) debe implementarse en un contenedor que administre la vista actual si es diferente de un control que proporciona la vista actual. Por ejemplo, Windows Explorer contiene un control de lista para el contenido de la carpeta actual, mientras que la vista del control se administra desde la aplicación Windows Explorer.
-   No se considera que un control que puede ordenar su contenido admita varias vistas.
-   La colección de vistas debe ser idéntica en todas las instancias.
-   Los nombres de vista deben ser adecuados para su uso en texto para voz, Legible y otras aplicaciones legibles.

## <a name="required-members-for-imultipleviewprovider"></a>Miembros necesarios para **IMultipleViewProvider**

Las siguientes propiedades y métodos son necesarios para implementar la [**interfaz IMultipleViewProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)



| Miembros requeridos                                                            | Tipo de miembro | Notas |
|-----------------------------------------------------------------------------|-------------|-------|
| [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | Propiedad.    | None  |
| [**GetSupportedViews**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | Método      | None  |
| [**GetViewName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | Método      | None  |
| [**SetCurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | Método      | None  |



 

Este patrón de control no tiene eventos asociados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Patrón de control ExpandCollapse](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




