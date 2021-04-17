---
description: Autenticación mediante tarjeta inteligente
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Autenticación mediante tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652937"
---
# <a name="smart-card-authentication"></a>Autenticación mediante tarjeta inteligente

Las partes básicas del [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md) se basan en los estándares PC/SC (consulte las especificaciones en [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ). Estas partes básicas incluyen:

-   Un [*Administrador de recursos*](../secgloss/r-gly.md) que usa una API de Windows.
-   Una [*interfaz de usuario*](../secgloss/u-gly.md) (IU) que funciona con el administrador de recursos.
-   Varios [*proveedores de servicios*](../secgloss/s-gly.md) base que proporcionan acceso a servicios específicos. A diferencia de la API de Windows de Resource Manager, los proveedores de servicios usan un modelo de interfaz COM para proporcionar servicios de [*tarjetas inteligentes*](../secgloss/s-gly.md) .

En la ilustración siguiente se muestran las relaciones de estos elementos en la arquitectura general de la tarjeta inteligente.

![arquitectura de tarjeta inteligente](images/smartovr2a.png)

Para obtener información acerca de cómo funciona el [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md) con otros servicios disponibles en Microsoft Internet Security Framework, consulte [relación con otros servicios](relation-to-other-services.md).

Para obtener información acerca de la autenticación mediante tarjeta inteligente, vea los temas siguientes.



| Temas                                                                      | Contenido                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Conceptos de tarjetas inteligentes](smart-card-concepts.md)<br/>                   | Conceptos básicos y descripción de la interacción entre los usuarios y las tarjetas inteligentes.<br/>                                                                                                                                                        |
| [Administrador de recursos de tarjeta inteligente](smart-card-resource-manager.md)<br/>   | Información acerca de la API de Resource Manager, que administra el acceso a los [*lectores*](../secgloss/r-gly.md) y a las [*tarjetas inteligentes*](../secgloss/s-gly.md).<br/> |
| [Interfaz de usuario de tarjeta inteligente](smart-card-user-interface.md)<br/>       | Información sobre el [*cuadro de diálogo común de tarjeta inteligente*](../secgloss/s-gly.md).<br/>                                                                                   |
| [Proveedores de servicios de tarjetas inteligentes](smart-card-service-providers.md)<br/> | Información acerca de las interfaces, los comandos y los contenedores que proporcionan capacidades de tarjetas inteligentes.<br/>                                                                                                                                              |



 

Además, los desarrollos actuales de tarjetas inteligentes de Microsoft se pueden encontrar en [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .

 

 
