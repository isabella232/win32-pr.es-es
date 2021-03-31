---
description: El protocolo Kerberos se compone de tres subprotocolos.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Subprotocolos Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277147"
---
# <a name="kerberos-subprotocols"></a>Subprotocolos Kerberos

El [*protocolo Kerberos*](../secgloss/k-gly.md) se compone de tres subprotocolos.



| Subprotocolo                                                                         | Significado                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intercambio del servicio de autenticación](authentication-service-exchange.md)<br/>   | En este subprotocolo, el [*centro de distribución de claves*](../secgloss/k-gly.md) (KDC) proporciona al cliente una [*clave de sesión*](../secgloss/s-gly.md) de inicio de sesión y un vale de concesión de vales (TGT).<br/> |
| [Intercambio del servicio de concesión de vales](ticket-granting-service-exchange.md)<br/> | En este subprotocolo, el KDC distribuye una clave de sesión de servicio y un vale para el servicio.<br/>                                                                                                                                                                                                            |
| [Intercambio de cliente/servidor](client-server-exchange.md)<br/>                     | En este subprotocolo, el cliente presenta el vale para la admisión a un servicio.<br/>                                                                                                                                                                                                                         |



 

 

 
