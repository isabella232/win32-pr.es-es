---
title: Acceso al almacén de reserva
description: La API del servidor HTTP mantiene la lista de reserva de espacio de nombres para todos los usuarios del equipo.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Acceso al almacén de reserva HTTP
- Almacén de reserva HTTP, acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418714"
---
# <a name="accessing-the-reservation-store"></a>Acceso al almacén de reserva

La API del servidor HTTP mantiene la lista de reserva de espacio de nombres para todos los usuarios del equipo. Una entrada de reserva consta de un [UrlPrefix](urlprefix-strings.md) y de la ACL correspondiente. Cada UrlPrefix del almacén tiene una ACL que enumera todos los usuarios que pueden registrarse para recibir solicitudes para el espacio de nombres. Los usuarios con privilegios de delegación pueden delegar subárboles del espacio de nombres que les pertenezcan a otros usuarios o eliminar reservas existentes mediante las API de configuración.

Para agregar una reserva al almacén de reserva persistente, la aplicación llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro de identificador de configuración establecido en el valor **HttpServiceConfigUrlAclInfo** . La API del servidor HTTP comprueba la propiedad del espacio de nombres y el ID. de usuario antes de agregar una reserva al almacén.

La API del servidor HTTP también proporciona funciones para consultar y eliminar las configuraciones del servicio para espacios de nombres de direcciones URL. La función [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) llamada con el parámetro de identificador de configuración establecida en las consultas de valor **HttpServiceConfigUrlAclInfo** , y la función [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) elimina en el almacén de espacios de nombres URL.

 

 




