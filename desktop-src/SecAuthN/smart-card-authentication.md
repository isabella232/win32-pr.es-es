---
description: Autenticación con tarjeta inteligente
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Autenticación con tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78bccfa9e762c137e332c26b5375584658c22718d336800b6dc73cf056ebde1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918016"
---
# <a name="smart-card-authentication"></a>Autenticación con tarjeta inteligente

Las partes básicas del subsistema [*de tarjetas inteligentes*](../secgloss/s-gly.md) se basan en estándares pc/SC (consulte las especificaciones en [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ). Estas partes básicas incluyen:

-   Un [*administrador de recursos*](../secgloss/r-gly.md) que usa Windows API.
-   Interfaz [*de usuario*](../secgloss/u-gly.md) (UI) que funciona con el administrador de recursos.
-   Varios proveedores [*de servicios base*](../secgloss/s-gly.md) que proporcionan acceso a servicios específicos. A diferencia de la API de Windows del administrador de recursos, los proveedores de servicios usan un modelo de interfaz COM para proporcionar servicios [*de tarjeta*](../secgloss/s-gly.md) inteligente.

En la ilustración siguiente se muestran las relaciones de estas partes en la arquitectura general de tarjetas inteligentes.

![arquitectura de tarjeta inteligente](images/smartovr2a.png)

Para obtener información sobre cómo funciona el [*subsistema de tarjetas*](../secgloss/s-gly.md) inteligentes con otros servicios disponibles en Microsoft Internet Security Framework, vea [Relación con otros servicios.](relation-to-other-services.md)

Para obtener información sobre la autenticación con tarjeta inteligente, consulte los temas siguientes.



| Temas                                                                      | Contenido                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Conceptos de tarjeta inteligente](smart-card-concepts.md)<br/>                   | Conceptos básicos y descripción de la interacción entre usuarios y tarjetas inteligentes.<br/>                                                                                                                                                        |
| [Tarjeta inteligente Resource Manager](smart-card-resource-manager.md)<br/>   | Información sobre la API de Resource Manager, que administra el acceso a los lectores [*y*](../secgloss/r-gly.md) a [*las tarjetas inteligentes.*](../secgloss/s-gly.md)<br/> |
| [Tarjeta inteligente Interfaz de usuario](smart-card-user-interface.md)<br/>       | Información sobre el [*cuadro de diálogo común de tarjeta inteligente*](../secgloss/s-gly.md).<br/>                                                                                   |
| [Proveedores de servicios de tarjeta inteligente](smart-card-service-providers.md)<br/> | Información sobre interfaces, comandos y contenedores que proporcionan funcionalidades de tarjeta inteligente.<br/>                                                                                                                                              |



 

Además, los desarrollos actuales de tarjetas inteligentes de Microsoft se pueden encontrar en [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .

 

 
