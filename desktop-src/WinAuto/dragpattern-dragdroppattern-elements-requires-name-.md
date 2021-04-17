---
title: Los elementos DragPattern/DragDropPattern requieren el nombre
description: Los elementos DragPattern/DragDropPattern requieren el nombre
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704565"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a>Los elementos DragPattern/DragDropPattern requieren el nombre

## <a name="text"></a>Texto

Los elementos que admiten arrastrar y colocar deben tener un conjunto ' name ' válido

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El elemento admite [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), pero no tiene un conjunto de nombres válido.

Este problema causa problemas para las personas que dependen de un lector de pantalla. El usuario no podrá indicar cuál es el objeto, ya que la lectura de pantalla no leerá un nombre válido para distinguir lo que es este elemento al arrastrar.

## <a name="possible-causes"></a>Causas posibles

-   El elemento, o su elemento primario, tiene un nombre o una etiqueta asignados incorrectamente.
-   Un desarrollador no es consciente de que los lectores de pantalla leen los nombres y los tipos de control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




