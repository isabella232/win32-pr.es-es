---
description: La función SetupSetSourceList abrirá o creará una lista de origen en el sistema de usuarios.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Uso de la lista de origen de MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1fa55a1c0defea2f344200eb331b8031dedfa66336510fb55b6fb77213a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100635"
---
# <a name="using-the-mru-source-list"></a>Uso de la lista de origen de MRU

La [**función SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) abrirá o creará una lista de origen en el sistema del usuario. Puede especificar para establecer la lista de usuarios, la lista del sistema, una combinación de las listas de usuarios y del sistema, o una lista temporal como lista de origen de MRU. Si se usa una lista temporal, será la única lista disponible para la aplicación de instalación hasta que se llame a [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) o se llame a **SetupSetSourceList** una segunda vez.

Una vez establecida una lista, puede consultar la lista de origen mediante [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) para obtener una matriz de las rutas de acceso de origen. Cuando la matriz de lista de origen ya no sea necesaria, debe llamar a la función [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) para liberar los recursos asignados por [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).

Para agregar una ruta de acceso a una lista de origen, ya sea una que esté residentes en el sistema del usuario o una lista temporal, llame a [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista). Si la lista de origen especificada no es temporal, ese origen permanecerá en el sistema del usuario y será accesible para las instalaciones posteriores.

Para quitar una ruta de acceso de la ruta de acceso de origen, llame a la [**función SetupRemoveFromSourceList.**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista)

 

 



