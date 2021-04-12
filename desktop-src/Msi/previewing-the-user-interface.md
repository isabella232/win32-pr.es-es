---
description: El instalador almacena toda la información sobre la interfaz de usuario en las tablas de la base de datos de instalación.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Obtener una vista previa de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277163"
---
# <a name="previewing-the-user-interface"></a>Obtener una vista previa de la interfaz de usuario

El instalador almacena toda la información sobre la [interfaz de usuario](user-interface.md) en las tablas de la base de datos de instalación. Para facilitar el diseño de la interfaz de usuario, el instalador también proporciona un modo de vista previa para ver esta información. En el procedimiento siguiente se describe cómo habilitar el modo de vista previa de la interfaz de usuario y mostrar la apariencia actual de cuadros de diálogo y cartelera.

**Para ver la interfaz de usuario en el modo de vista previa**

1.  Habilite el modo de vista previa mediante una llamada a la función [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) .
2.  Para mostrar los cuadros de diálogo concretos, llame a la función [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) .
3.  Mostrar una cartelera determinada mediante una llamada a la función [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) .

 

 



