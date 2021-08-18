---
title: Acceso al almacén de reservas
description: La API del servidor HTTP mantiene la lista de reservas de espacios de nombres para todos los usuarios del equipo.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Acceso al HTTP del Almacén de reservas
- Almacén de reservas HTTP, acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f9244fd4513517793bf85d205308fc49ac2d8ca0a246c17a68c730d1c76168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015023"
---
# <a name="accessing-the-reservation-store"></a>Acceso al almacén de reservas

La API del servidor HTTP mantiene la lista de reservas de espacios de nombres para todos los usuarios del equipo. Una entrada de reserva consta de [UrlPrefix](urlprefix-strings.md) y la ACL correspondiente. Cada UrlPrefix del almacén tiene una ACL que enumera todos los usuarios a los que se les permite registrarse para recibir solicitudes para el espacio de nombres. Los usuarios con privilegios de delegación pueden delegar subárboles del espacio de nombres que poseen a otros usuarios o eliminar las reservas existentes mediante las API de configuración.

Para agregar una reserva al almacén de reservas persistente, la aplicación llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro de identificador de configuración establecido en el **valor HttpServiceConfigUrlAclInfo.** La API del servidor HTTP comprueba la propiedad del espacio de nombres y el identificador de usuario antes de agregar una reserva al almacén.

La API del servidor HTTP también proporciona funciones para consultar y eliminar las configuraciones de servicio de los espacios de nombres de dirección URL. La función [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) a la que se llama con el parámetro de identificador de configuración establecido en las consultas de valor **HttpServiceConfigUrlAclInfo** y la función [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) se elimina en el almacén de espacios de nombres url.

 

 




