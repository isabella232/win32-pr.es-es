---
title: Obtención de SLO de servicio y usuario
description: Para obtener STO para NPS (IAS) o un usuario determinado, llame a los métodos ISdoMachine GetServiceSDO o ISdoMachine GetUserSDO.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebef1e695236bd1449ab886cb998a67f09c2cafc8ded446b0b7e1ad89b01181
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128595"
---
# <a name="obtaining-service-and-user-sdos"></a>Obtención de SLO de servicio y usuario

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se cambió a Servidor de directivas de red (NPS) a partir Windows Server 2008.

 

Para obtener STO para NPS (IAS) o un usuario determinado, llame a los [**métodos ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine::GetUserSDO.**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) Estos métodos devuelven punteros a interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para estos objetos. Para el SDO del usuario, use el [**método IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener una [**interfaz ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para el objeto . Para el SDO del servicio, use **IUnknown::QueryInterface** para obtener una [**interfaz ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) o [**ISdoServiceControl.**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)

Antes de llamar a [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine::GetUserSDO,**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)llame a [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) para asociar el objeto de máquina con el equipo local.

Consulte [Recuperación de un SDO de](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) servicio y Recuperación de un [SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) de usuario para obtener código de ejemplo que muestra cómo obtener estos STO.

 

 