---
description: La interfaz IUpdateSearcher define las siguientes propiedades.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Propiedades de IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/11/2021
ms.locfileid: "104362402"
---
# <a name="iupdatesearcher-properties"></a>Propiedades de IUpdateSearcher

La interfaz [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) define las siguientes propiedades.



| Propiedad                                                                                           | Descripción                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutomaticallyUpgradeService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | Obtiene y establece un valor booleano que indica si las futuras llamadas a los métodos [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) y [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) dan como resultado una actualización automática a Windows Update Agent (WUA). |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Identifica la aplicación cliente actual.                                                                                                                                                                                                   |
| [**IncludePotentiallySupersededUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Obtiene y establece un valor booleano que indica si los resultados de la búsqueda incluyen actualizaciones reemplazadas por otras actualizaciones en los resultados de la búsqueda.                                                                                          |
| [**En línea**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Obtiene y establece un valor booleano que indica si [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) se conecta para buscar actualizaciones.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | Obtiene y establece un sitio en el que buscar cuando el sitio que se va a buscar no es un sitio Windows Update.                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Obtiene y establece un valor de [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) que indica el servidor en el que se van a buscar actualizaciones.                                                                                                                            |




 

 

 



