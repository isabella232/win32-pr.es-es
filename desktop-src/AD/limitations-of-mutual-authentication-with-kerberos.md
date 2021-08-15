---
title: Limitaciones de la autenticación mutua con Kerberos
description: Tanto la cuenta del cliente como la cuenta del servicio deben estar en Windows 2000 dominios nativos o en modo mixto porque los servicios kerberos no están disponibles en dominios de nivel inferior.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77bdc2f8cfe87d3cece32987ee0958000b1186775257013ce27f5950c6ac8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187069"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>Limitaciones de la autenticación mutua con Kerberos

Tanto la cuenta del cliente como la cuenta del servicio deben estar en Windows 2000 dominios nativos o en modo mixto porque los servicios kerberos no están disponibles en dominios de nivel inferior. Además, las cuentas de cliente y de servicio deben estar en el mismo bosque porque el KDC del cliente usa el catálogo global para buscar el nombre de la entidad de servicio.

Tanto el servicio como el cliente deben ejecutarse en Windows 2000; de lo contrario, se producirá un error en la autenticación mutua con Kerberos porque las versiones anteriores de Windows no admiten Kerberos.

Los nombres de entidad de seguridad de servicio deben incluir el nombre DNS del servidor host en el que se ejecuta el servicio. Debe usar el nombre DNS.

 

 




