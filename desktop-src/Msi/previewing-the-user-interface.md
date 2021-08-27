---
description: El instalador almacena toda la información sobre la interfaz de usuario en las tablas de la base de datos de instalación.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Vista previa de la Interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738387ac834d4e9c26f4a413755dce0c5abdc5e421cc4ef88b1f9b41054f201d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082665"
---
# <a name="previewing-the-user-interface"></a>Vista previa de la Interfaz de usuario

El instalador almacena toda la información sobre la [interfaz de usuario en](user-interface.md) las tablas de la base de datos de instalación. Para facilitar el diseño de la interfaz de usuario, el instalador también proporciona un modo de vista previa para ver esta información. En el procedimiento siguiente se describe cómo habilitar el modo de vista previa de la interfaz de usuario y mostrar la apariencia actual de cuadros de diálogo y paneles.

**Para ver la interfaz de usuario en modo de vista previa**

1.  Habilite el modo de vista previa mediante una llamada [**a la función MsiEnableUIPreview.**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
2.  Para mostrar los cuadros de diálogo concretos, llame a [**la función MsiPreviewDialog.**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
3.  Muestre determinados paneles mediante una llamada a [**la función MsiPreviewBillboard.**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)

 

 



