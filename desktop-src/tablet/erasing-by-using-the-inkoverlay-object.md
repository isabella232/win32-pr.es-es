---
description: El objeto InkOverlay se puede adjuntar a un control de ventana y se usa para habilitar la capacidad básica de entrada de lápiz.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Borrar mediante el objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf85926f3566340cbde0d3202f3485e7c54cccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810087"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>Borrar mediante el objeto InkOverlay

El objeto [**InkOverlay**](inkoverlay-class.md) se puede adjuntar a un control de ventana y se usa para habilitar la capacidad básica de entrada de lápiz. Puede usar el objeto **InkOverlay** para borrar la entrada de lápiz; para ello, establezca la propiedad [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) en **Delete**. Después, puede establecer la propiedad [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) en los miembros de **trazo** o **punto** de [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode). Al establecer la propiedad **EraserMode** en **Stroke** , se borran los trazos completos. Al establecer la propiedad **EraserMode** en **Point** , se borra la tinta que pasa el cursor.

 

 



