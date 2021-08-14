---
description: Los proveedores de servicios de tarjeta inteligente (SCSP) proporcionan acceso a las funcionalidades de tarjeta inteligente.
ms.assetid: f214385f-3e65-4175-925c-3d1dc4060185
title: Proveedores de servicios de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57cd16787985a1e8f92105ce61aed4b9532bff806aabb7d8ad4bdd407d807014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917389"
---
# <a name="smart-card-service-providers"></a>Proveedores de servicios de tarjeta inteligente

Los proveedores de servicios de tarjeta inteligente (SCSP) proporcionan acceso a las [*funcionalidades de tarjeta*](../secgloss/s-gly.md) inteligente. Pueden proporcionar acceso a una sola funcionalidad, como los proveedores de servicios base proporcionados por el SDK de tarjeta inteligente, o pueden proporcionar acceso a varias funcionalidades para realizar una tarea más compleja.

Los proveedores de servicios proporcionan acceso a través de interfaces COM. El SDK de tarjeta inteligente proporciona las interfaces COM que usan sus propios proveedores de servicios base, así como varias interfaces de aplicación que se pueden usar al desarrollar proveedores de servicios personalizados.



| Tema                                                                                   | Descripción                                            |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Proveedores de servicios base](base-service-providers.md)<br/>                         | Proveedores de servicios base.<br/>                     |
| [Creación de un comando APDU ISO7816-4](building-an-iso7816-4-apdu-command.md)<br/> | Agregar funcionalidad a un proveedor de servicios.<br/> |
| [Proveedor de servicios contenedor de proveedor](vendor-wrapper-service-provider.md)<br/>       | Un ejemplo de contenedor de proveedor.<br/>                   |



 

Para obtener información general de todas las interfaces COM proporcionadas por el SDK de tarjeta inteligente (proveedor de servicios base e interfaces de aplicación), vea [Interfaces de tarjeta inteligente](smart-card-interfaces.md).

 

 
