---
description: Este cuadro de diálogo modal permite a los usuarios seleccionar elementos concretos.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Cuadro de diálogo Selección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5876f6015631d175bd22e342db17788d468038e4a999aa78ae5a3a33fd028c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040705"
---
# <a name="selection-dialog"></a>Cuadro de diálogo Selección

Este cuadro de diálogo modal permite a los usuarios seleccionar elementos concretos.

Un cuadro de diálogo Selección contiene un [control SelectionTree](selectiontree-control.md) que publica varios controles ControlEvents. Normalmente, estos controles ControlEvents se suscriben mediante controles [Text](text-control.md), [Icon](icon-control.md)o [Bitmap](bitmap-control.md) que muestran una descripción, el tamaño, la ruta de acceso y el icono del elemento resaltado.

Hay un [control PushButton en](pushbutton-control.md) el cuadro de diálogo que publica [selectionBrowse ControlEvent](selectionbrowse-controlevent.md) y genera un [cuadro de diálogo Examinar](browse-dialog.md). El control Examinar permite al usuario seleccionar un directorio.

El árbol de selección se rellena solo después de llamar a la acción [CostInitialize](costinitialize-action.md) y a la acción [CostFinalize.](costfinalize-action.md)

Normalmente, se usa un cuadro de diálogo Selección para seleccionar características. Las características se enumeran como elementos en un control SelectionTree y se etiquetan con la cadena corta de texto que aparece en la columna Título de la [tabla Característica](feature-table.md). La cadena de texto de la columna Description de la tabla Feature se publica como [SelectionDescription ControlEvent](selectiondescription-controlevent.md) y se muestra mediante un [control Text](text-control.md) en el cuadro de diálogo Selección. El control de árbol Selección también publica el identificador en el icono del elemento resaltado.

 

 



