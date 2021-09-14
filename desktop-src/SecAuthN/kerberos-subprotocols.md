---
description: El protocolo Kerberos se compone de tres subprotocolos.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Subprotocolos kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073770"
---
# <a name="kerberos-subprotocols"></a>Subprotocolos kerberos

El [*protocolo Kerberos*](../secgloss/k-gly.md) se compone de tres subprotocolos.



| Subprotocolo                                                                         | Significado                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intercambio del servicio de autenticación](authentication-service-exchange.md)<br/>   | En este subprotocolo, el [*Centro de distribución de claves*](../secgloss/k-gly.md) (KDC) proporciona [](../secgloss/s-gly.md) al cliente una clave de sesión de inicio de sesión y un vale de concesión de vales (TGT).<br/> |
| [Intercambio del servicio de concesión de vales](ticket-granting-service-exchange.md)<br/> | En este subprotocolo, el KDC distribuye una clave de sesión de servicio y un vale para el servicio.<br/>                                                                                                                                                                                                            |
| [Cliente/servidor Exchange](client-server-exchange.md)<br/>                     | En este subprotocolo, el cliente presenta el vale para la admisión a un servicio.<br/>                                                                                                                                                                                                                         |



 

 

 
