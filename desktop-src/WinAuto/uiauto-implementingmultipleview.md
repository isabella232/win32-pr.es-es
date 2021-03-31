---
title: Patrón de control MultipleView
description: Describe las directrices y convenciones para implementar IMultipleViewProvider, incluida información sobre propiedades y métodos.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control MultipleView
- Automatización de la interfaz de usuario, patrón de control MultipleView
- Automatización de la interfaz de usuario, IMultipleViewProvider
- IMultipleViewProvider
- implementación de patrones de control MultipleView de UI Automation
- Patrones de control de MultipleView
- patrones de control, IMultipleViewProvider
- patrones de control, implementar la automatización de la interfaz de usuario MultipleView
- patrones de control, MultipleView
- interfaces, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418845"
---
# <a name="multipleview-control-pattern"></a>Patrón de control MultipleView

Describe las directrices y convenciones para implementar [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), incluida información sobre propiedades y métodos. Al final del tema se ofrecen vínculos a referencias adicionales. El patrón de control **MultipleView** se usa para admitir controles que proporcionan y pueden cambiar entre varias representaciones de la misma información o el mismo conjunto de controles secundarios.

Algunos ejemplos de controles que pueden presentar varias vistas son la vista de lista (que puede mostrar su contenido como miniaturas, mosaicos, iconos o detalles), gráficos de Microsoft Excel (circular, línea, barra, valor de celda con una fórmula), documentos de Microsoft Word (normal, diseño web, diseño de impresión, diseño de lectura, esquema), calendario de Microsoft Outlook (año, mes, semana, día) y máscaras de Media Player de Microsoft Windows. Las vistas admitidas las determina el desarrollador del control y son específicas de cada control.

En este tema se incluyen las siguientes secciones.

-   [Directrices y convenciones de implementación](#implementation-guidelines-and-conventions)
-   [Miembros requeridos para **IMultipleViewProvider**](#required-members-for-imultipleviewprovider)
-   [Temas relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Directrices y convenciones de implementación

Al implementar el patrón de control **MultipleView** , tenga en cuenta las siguientes directrices y convenciones:

-   [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) también se debe implementar en un contenedor que administre la vista actual si es diferente de un control que proporciona la vista actual. Por ejemplo, el explorador de Windows contiene un control de lista para el contenido de la carpeta actual mientras que la vista del control se administra desde la aplicación del explorador de Windows.
-   No se considera que un control que puede ordenar su contenido admita varias vistas.
-   La colección de vistas debe ser idéntica en todas las instancias.
-   Los nombres de vista deben ser adecuados para su uso en texto a voz, Braille y otras aplicaciones legibles para el usuario.

## <a name="required-members-for-imultipleviewprovider"></a>Miembros requeridos para **IMultipleViewProvider**

Se requieren las siguientes propiedades y métodos para implementar la interfaz [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) .



| Miembros requeridos                                                            | Tipo de miembro | Notas |
|-----------------------------------------------------------------------------|-------------|-------|
| [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | Propiedad    | None  |
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

 

 




