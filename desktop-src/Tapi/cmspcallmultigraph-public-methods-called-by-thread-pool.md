---
description: La lista siguiente contiene los métodos públicos CMSPCallMultiGraph llamados por el grupo de subprocesos.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: CMSPCallMultiGraph métodos públicos, llamado por el grupo de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677945"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a>CMSPCallMultiGraph métodos públicos, llamado por el grupo de subprocesos



| Métodos públicos de CMSPCallMultiGraph                                   | Descripción                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | Se llama cuando el gráfico de filtro señala un evento.                                                                                                                                                           |
| [**HandleGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | Llamado por el método estático [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) . Pone en cola [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) en el subproceso de trabajo MSP principal. |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | Permite que la instancia del objeto de llamada MSP controle el evento de gráfico de filtro.                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



