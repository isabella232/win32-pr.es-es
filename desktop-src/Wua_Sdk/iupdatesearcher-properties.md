---
description: La interfaz IUpdateSearcher define las siguientes propiedades.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Propiedades de IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dc3af2635fff4260a44261333b23cbfcf1661793ad613f08bb288db452b93d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130437"
---
# <a name="iupdatesearcher-properties"></a>Propiedades de IUpdateSearcher

La [**interfaz IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) define las siguientes propiedades.



| Propiedad                                                                                           | Descripción                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutomaticallyUpgradeService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | Obtiene y establece un valor booleano que indica si las llamadas futuras a los métodos [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) y [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) darán lugar a una actualización automática a Windows Update Agent (WUA). |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Identifica la aplicación cliente actual.                                                                                                                                                                                                   |
| [**IncludePotentiallySupersedUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Obtiene y establece un valor booleano que indica si los resultados de la búsqueda incluyen actualizaciones reemplazadas por otras actualizaciones en los resultados de búsqueda.                                                                                          |
| [**En línea**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Obtiene y establece un valor booleano que indica si [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) se pone en línea para buscar actualizaciones.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | Obtiene y establece un sitio en el que buscar cuando el sitio en el que se va a buscar no es Windows sitio de actualización.                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Obtiene y establece un [**valor ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) que indica el servidor en el que se buscarán actualizaciones.                                                                                                                            |




 

 

 



