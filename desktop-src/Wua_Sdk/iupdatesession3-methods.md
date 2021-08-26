---
description: La interfaz IUpdateSession3 define los métodos siguientes.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Métodos IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845af7bc4858aa713a3c044562c91325d337e49da0f413a3b2536c0129a85bc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896745"
---
# <a name="iupdatesession3-methods"></a>Métodos IUpdateSession3

La [**interfaz IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) define los métodos siguientes.



| Método                                                                           | Descripción                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpdateServiceManager**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | Devuelve un puntero a una [**interfaz IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) para la sesión.                                                                                                                                                                                                                |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | Devuelve un puntero a una [**interfaz IUpdateHistoryEntryCollection.**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) La interfaz contiene registros de eventos que coinciden en el equipo. Esto hace que [**el método QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) consulte sincrónicamente el equipo para el historial de eventos de actualización. |



 

Para obtener información sobre los miembros heredados por esta interfaz, vea las interfaces siguientes:

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



