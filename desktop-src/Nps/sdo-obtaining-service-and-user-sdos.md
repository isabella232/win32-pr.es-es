---
title: Obtención del servicio y el usuario SDOs
description: Para obtener SDOs para NPS (IAS) o un usuario determinado, llame a los métodos ISdoMachine GetServiceSDO o ISdoMachine GetUserSDO.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359166"
---
# <a name="obtaining-service-and-user-sdos"></a>Obtención del servicio y el usuario SDOs

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.

 

Para obtener SDOs para NPS (IAS) o un usuario determinado, llame a los métodos [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) . Estos métodos devuelven punteros a las interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para estos objetos. Para el SDO de usuarios, use el método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener una interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para el objeto. En el caso de los SDO de servicio, use **IUnknown:: QueryInterface** para obtener una interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) o una interfaz [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .

Antes de llamar a [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), llame a [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) para asociar el objeto de equipo al equipo local.

Vea [recuperar un SDO de servicio](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) y [recuperar un SDO de usuarios](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) para obtener código de ejemplo que muestra cómo obtener estos SDOs.

 

 