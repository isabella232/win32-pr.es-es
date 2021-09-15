---
description: El instalador almacena toda la información sobre la interfaz de usuario en las tablas de la base de datos de instalación.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Vista previa de la Interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473955"
---
# <a name="previewing-the-user-interface"></a>Vista previa de la Interfaz de usuario

El instalador almacena toda la información sobre la interfaz [de usuario en](user-interface.md) las tablas de la base de datos de instalación. Para facilitar el diseño de la interfaz de usuario, el instalador también proporciona un modo de vista previa para ver esta información. En el procedimiento siguiente se describe cómo habilitar el modo de vista previa de la interfaz de usuario y mostrar la apariencia actual de los cuadros de diálogo y los paneles.

**Para ver la interfaz de usuario en el modo de vista previa**

1.  Habilite el modo de vista previa mediante una llamada [**a la función MsiEnableUIPreview.**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
2.  Para mostrar los cuadros de diálogo concretos, llame a [**la función MsiPreviewDialog.**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
3.  Para mostrar determinados paneles, llame a [**la función MsiPreviewBillboard.**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)

 

 



