---
description: Este cuadro de diálogo modal permite a los usuarios seleccionar elementos determinados.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Cuadro de diálogo de selección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653082"
---
# <a name="selection-dialog"></a>Cuadro de diálogo de selección

Este cuadro de diálogo modal permite a los usuarios seleccionar elementos determinados.

Un cuadro de diálogo de selección contiene un [control SelectionTree](selectiontree-control.md) que publica varios ControlEvents. Normalmente, estos ControlEvents se suscriben a mediante controles de [texto](text-control.md), [icono](icon-control.md)o [mapa de bits](bitmap-control.md) que muestran una descripción, el tamaño, la ruta de acceso y el icono del elemento resaltado.

Hay un [control Pushbutton](pushbutton-control.md) en el cuadro de diálogo que publica [SelectionBrowse ControlEvent,](selectionbrowse-controlevent.md) y genera un [cuadro de diálogo de exploración](browse-dialog.md). El control de exploración permite al usuario seleccionar un directorio.

El árbol de selección se rellena solo después de que se llame a la acción [CostInitialize](costinitialize-action.md) y a la [acción CostFinalize](costfinalize-action.md) .

Un cuadro de diálogo de selección se usa normalmente para seleccionar características. Las características se enumeran como elementos en un control SelectionTree y se etiquetan con la cadena corta de texto que aparece en la columna title de la [tabla de características](feature-table.md). La cadena de texto de la columna Descripción de la tabla de características se publica como [SelectionDescription ControlEvent,](selectiondescription-controlevent.md) y se muestra en un [control de texto](text-control.md) en el cuadro de diálogo de selección. El control de árbol de selección también publica el identificador en el icono del elemento resaltado.

 

 



