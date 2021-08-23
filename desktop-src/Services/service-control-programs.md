---
description: Un programa de control de servicio inicia y controla los servicios.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programas de control de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb11e8224a23edcebd0688039502c5bc38da929d47cba470e6f397f4430e444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889048"
---
# <a name="service-control-programs"></a>Programas de control de servicio

Un programa de control de servicio inicia y controla los servicios. Las acciones que realiza son las siguientes:

-   Inicia un servicio o servicio de controlador, si el tipo de inicio es SERVICE \_ DEMAND \_ START.
-   Envía solicitudes de control a un servicio en ejecución.
-   Consulta el estado actual de un servicio en ejecución.

Estas acciones requieren un identificador abierto para el objeto de servicio. Para obtener el identificador, el programa de control de servicio debe:

1.  Use la [**función OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para obtener un identificador para la base de datos de SCM en un equipo especificado.
2.  Use las [**funciones OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) [**o CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obtener un identificador para el objeto de servicio.

Para obtener más información, vea los temas siguientes:

-   [Inicio del servicio](service-startup.md)
-   [Solicitudes de control de servicio](service-control-requests.md)
-   [Controlar un servicio mediante SC](controlling-a-service-using-sc.md)

 

 



