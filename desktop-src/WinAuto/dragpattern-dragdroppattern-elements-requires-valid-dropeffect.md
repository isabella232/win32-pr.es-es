---
title: Los elementos DragPattern/DragDropPattern requieren DropEffect válido
description: Los elementos DragPattern/DragDropPattern requieren DropEffect válido
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772702"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>Los elementos DragPattern/DragDropPattern requieren DropEffect válido

## <a name="text"></a>Texto

Los elementos que admiten arrastrar y colocar deben tener un conjunto ' DropEffect ' válido

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

El elemento admite [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), pero no tiene un conjunto de propiedades [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) válido.

Este problema causa problemas para las personas que dependen de un lector de pantalla. El usuario no podrá saber qué efecto tiene este objeto al arrastrar.

## <a name="possible-causes"></a>Causas posibles

-   El elemento, o su elemento primario, no ha creado el [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) o [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) un nombre o una etiqueta asignados de forma incorrecta.
-   Un desarrollador no es consciente de que los lectores de pantalla lean DropEffect (s).

 

 




