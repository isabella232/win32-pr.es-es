---
title: Direcciones IP y nombres de equipo
description: No es seguro suponer que el nombre del equipo o la dirección IP que se asignen al equipo se asocian a un único usuario, dado que varios usuarios pueden iniciar sesión a la vez en un servidor host de sesión de Escritorio remoto.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168682"
---
# <a name="ip-addresses-and-computer-names"></a>Direcciones IP y nombres de equipo

Varios usuarios pueden iniciar sesión simultáneamente en un Escritorio remoto host de sesión de escritorio remoto. Por lo tanto, no es seguro suponer que el nombre del equipo o la dirección IP asignada al equipo están asociados a un solo usuario. Esto difiere de un entorno de Windows usuario único, en el que solo un usuario inicia sesión a la vez.

Las aplicaciones que usan el nombre de equipo o la dirección IP para la concesión de licencias o como medio para identificar una iteración de la aplicación en la red no funcionarán correctamente en un entorno de Servicios de Escritorio remoto, ya que el nombre de equipo o la dirección IP del servidor se pueden asociar a muchos usuarios.

En un Servicios de Escritorio remoto, cada terminal cliente o emulador de terminal tiene una dirección IP y un nombre de equipo independientes. Para recuperar la dirección IP y el nombre de equipo de un cliente, llame a la [**función WTSQuerySessionInformation.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) Otras funciones que recuperan estas direcciones de red y nombres de equipo recuperan el nombre y la dirección del servidor host de sesión de Escritorio remoto. Por ejemplo, la [**función GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) devuelve el nombre de equipo del servidor.

 

 