---
title: Los elementos DragPattern/DragDropPattern requieren dropEffect válido
description: Los elementos DragPattern/DragDropPattern requieren dropEffect válido
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd95e1da2d3d05c7499f72c86d454da2832947cafd0150e8f62b2f3e8d56af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115683"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>Los elementos DragPattern/DragDropPattern requieren dropEffect válido

## <a name="text"></a>Texto

Los elementos que admiten arrastrar y colocar deben tener un conjunto 'DropEffect' válido

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El elemento admite [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern)pero no tiene un conjunto de propiedades [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) válido.

Este problema provoca problemas para las personas que dependen de un lector de pantalla. El usuario no podrá saber qué efecto tiene este objeto al arrastrar.

## <a name="possible-causes"></a>Causas posibles

-   El elemento , o su elemento primario, no ha creado [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) o [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) un nombre o etiqueta asignados incorrectamente.
-   Un desarrollador no es consciente de que los lectores de pantalla leen DropEffect.s.

 

 




