---
description: El protocolo Kerberos se compone de tres subprotocolos.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Subprotocolos kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ea1ababaf1ec7fe4e80112d4c1f69dc8bfc242a40cea56675d08198188a130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013365"
---
# <a name="kerberos-subprotocols"></a>Subprotocolos kerberos

El [*protocolo Kerberos*](../secgloss/k-gly.md) se compone de tres subprotocolos.



| Subprotocolo                                                                         | Significado                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intercambio del servicio de autenticación](authentication-service-exchange.md)<br/>   | En este subprotocolo, el Centro de distribución de claves (KDC) proporciona [](../secgloss/s-gly.md) al cliente una clave de sesión de inicio de sesión y un vale de concesión de vales (TGT). [](../secgloss/k-gly.md)<br/> |
| [Intercambio del servicio de concesión de vales](ticket-granting-service-exchange.md)<br/> | En este subprotocolo, el KDC distribuye una clave de sesión de servicio y un vale para el servicio.<br/>                                                                                                                                                                                                            |
| [Cliente/servidor Exchange](client-server-exchange.md)<br/>                     | En este subprotocolo, el cliente presenta el vale para la admisión a un servicio.<br/>                                                                                                                                                                                                                         |



 

 

 
