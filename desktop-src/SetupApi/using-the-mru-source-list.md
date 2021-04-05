---
description: La función SetupSetSourceList abrirá o creará una lista de origen en el sistema de usuarios.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Usar la lista de origen de MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbecb9e32a554d1818661b1fd7f6e782744c16e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001638"
---
# <a name="using-the-mru-source-list"></a>Usar la lista de origen de MRU

La función [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) abrirá o creará una lista de origen en el sistema del usuario. Puede especificar para establecer la lista de usuarios, la lista de sistemas, una combinación de las listas de usuarios y del sistema, o una lista temporal como la lista de origen de MRU. Si se usa una lista temporal, será la única lista disponible para la aplicación de instalación hasta que se llame a [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) o se llame a **SetupSetSourceList** por segunda vez.

Una vez establecida una lista, puede consultar la lista de origen mediante [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) para obtener una matriz de las rutas de acceso de origen. Cuando la matriz de la lista de origen ya no sea necesaria, debe llamar a la función [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) para liberar los recursos asignados por [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).

Para agregar una ruta de acceso a una lista de origen, ya sea una que sea residente en el sistema del usuario o una lista temporal, llame a [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista). Si la lista de origen especificada no es temporal, el origen permanecerá en el sistema del usuario y será accesible para las instalaciones posteriores.

Para quitar una ruta de acceso de la ruta de origen, llame a la función [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .

 

 



