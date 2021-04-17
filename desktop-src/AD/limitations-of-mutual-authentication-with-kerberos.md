---
title: Limitaciones de la autenticación mutua con Kerberos
description: Tanto la cuenta del cliente como la cuenta del servicio deben estar en dominios de modo nativo o mixto de Windows 2000, ya que los servicios de Kerberos no están disponibles en los dominios de nivel inferior.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486591"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>Limitaciones de la autenticación mutua con Kerberos

Tanto la cuenta del cliente como la cuenta del servicio deben estar en dominios de modo nativo o mixto de Windows 2000, ya que los servicios de Kerberos no están disponibles en los dominios de nivel inferior. Además, las cuentas de cliente y de servicio deben estar en el mismo bosque porque el KDC del cliente usa el catálogo global para buscar el nombre de la entidad de seguridad de servicio.

Tanto el servicio como el cliente deben ejecutarse en Windows 2000, de lo contrario, se producirá un error en la autenticación mutua con Kerberos porque las versiones anteriores de Windows no admiten Kerberos.

Los nombres de entidad de seguridad de servicio deben incluir el nombre DNS del servidor host en el que se está ejecutando el servicio. Debe usar el nombre DNS.

 

 




