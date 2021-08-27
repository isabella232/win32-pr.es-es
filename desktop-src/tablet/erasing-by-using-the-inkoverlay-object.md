---
description: El objeto InkOverlay se puede adjuntar a un control de ventana y se usa para habilitar la funcionalidad de entrada de lápiz básica.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Borrado mediante el uso del objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6d95e7939bc53c534d3bfc9a542e40b95fbce05234000e24b107f0f2625eae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110945"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>Borrado mediante el uso del objeto InkOverlay

El [**objeto InkOverlay**](inkoverlay-class.md) se puede adjuntar a un control de ventana y se usa para habilitar la funcionalidad de entrada de lápiz básica. Puede usar el objeto **InkOverlay** para borrar la entrada de lápiz estableciendo la [**propiedad EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) en **Delete**. A continuación, puede establecer [**la propiedad EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) en los miembros **Stroke** o **Point** de [**InkOverlay ManualeserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode). Al establecer **la propiedad EraserMode** en **Trazo,** se borran trazos completos. Si se **establece la propiedad EraserMode** en **Point,** se borra la entrada de lápiz que pasa el cursor.

 

 



