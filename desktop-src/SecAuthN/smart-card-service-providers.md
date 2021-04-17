---
description: Los proveedores de servicios de tarjeta inteligente (SCSP) proporcionan acceso a las capacidades de las tarjetas inteligentes.
ms.assetid: f214385f-3e65-4175-925c-3d1dc4060185
title: Proveedores de servicios de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc60e9987912426fcca3f6605b9218e085e61ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652933"
---
# <a name="smart-card-service-providers"></a>Proveedores de servicios de tarjetas inteligentes

Los proveedores de servicios de tarjeta inteligente (SCSP) proporcionan acceso a las capacidades de las [*tarjetas inteligentes*](../secgloss/s-gly.md) . Pueden proporcionar acceso a una única funcionalidad, como los proveedores de servicios base proporcionados por el SDK de tarjeta inteligente, o bien pueden proporcionar acceso a varias funcionalidades para realizar una tarea más compleja.

Los proveedores de servicios proporcionan acceso a través de interfaces COM. El SDK de tarjeta inteligente proporciona las interfaces COM que usan sus propios proveedores de servicios base, así como varias interfaces de aplicación que se pueden usar al desarrollar proveedores de servicios personalizados.



| Tema                                                                                   | Descripción                                            |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Proveedores de servicios base](base-service-providers.md)<br/>                         | Proveedores de servicios base.<br/>                     |
| [Compilar un comando de APDU ISO7816-4](building-an-iso7816-4-apdu-command.md)<br/> | Agregar funcionalidad a un proveedor de servicios.<br/> |
| [Proveedor de servicios de contenedor de proveedores](vendor-wrapper-service-provider.md)<br/>       | Un ejemplo de contenedor de proveedores.<br/>                   |



 

Para obtener información general de todas las interfaces COM que proporciona el SDK de tarjeta inteligente (proveedor de servicios base e interfaces de aplicación), consulte [interfaces de tarjeta inteligente](smart-card-interfaces.md).

 

 
