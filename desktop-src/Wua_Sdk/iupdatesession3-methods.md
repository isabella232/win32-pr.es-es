---
description: La interfaz IUpdateSession3 define los siguientes métodos.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Métodos IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153825"
---
# <a name="iupdatesession3-methods"></a>Métodos IUpdateSession3

La interfaz [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) define los siguientes métodos.



| Método                                                                           | Descripción                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpdateServiceManager**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | Devuelve un puntero a una interfaz [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) para la sesión.                                                                                                                                                                                                                |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | Devuelve un puntero a una interfaz [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) . La interfaz contiene registros de eventos coincidentes en el equipo. Esto hace que el método [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) consulte de forma sincrónica el equipo para consultar el historial de eventos de actualización. |



 

Para obtener información sobre los miembros heredados por esta interfaz, vea las siguientes interfaces:

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



