---
description: El sistema usa la información de configuración para determinar cómo iniciar el servicio.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Configuración de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168897"
---
# <a name="service-configuration"></a>Configuración de servicio

El sistema usa la información de configuración para determinar cómo iniciar el servicio. La información de configuración también incluye el nombre para mostrar del servicio y su descripción. Por ejemplo, para el servicio DHCP, podría usar el nombre para mostrar "Servicio de protocolo de configuración dinámica de host" y la descripción "Proporciona direcciones de Internet para el equipo de la red".

Para modificar la información de configuración de un objeto de servicio, un programa de configuración usa la [**función ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) [**o ChangeServiceConfig2.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) Para obtener un ejemplo, vea [Cambiar una configuración de servicio.](changing-a-service-configuration.md)

Para recuperar la información de configuración de un objeto de servicio, el programa de configuración usa la [**función QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) o [**QueryServiceConfig2.**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) Para obtener un ejemplo, [vea Consulta de la configuración de un servicio.](querying-a-service-s-configuration.md)

Las funciones de configuración del servicio [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) [**y QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) admiten el uso de desencadenadores para controlar el inicio del servicio.

Para modificar el descriptor de seguridad para un objeto SCManager o un objeto de servicio, un programa de configuración usa la [**función SetServiceObjectSecurity.**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) Para recuperar una copia del descriptor de seguridad, el programa de configuración usa la [**función QueryServiceObjectSecurity.**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de un servicio mediante SC](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
