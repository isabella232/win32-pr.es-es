---
description: Los programadores y administradores del sistema usan programas de configuración de servicio para modificar o consultar la base de datos de los servicios instalados.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programas de configuración de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad7ef3efffb185b2d29c6eab496bf76d12343a0e16f845702e910695220b048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967709"
---
# <a name="service-configuration-programs"></a>Programas de configuración de servicio

Los programadores y administradores del sistema usan programas de configuración de servicio para modificar o consultar la base de datos de los servicios instalados. También se puede acceder a la base de datos mediante las funciones del Registro. Sin embargo, solo debe usar las funciones de configuración de SCM, que garantizan que el servicio está instalado y configurado correctamente.

Las funciones de configuración de SCM requieren un identificador para un objeto SCManager o un identificador para un objeto de servicio. Para obtener estos identificadores, el programa de configuración de servicio debe:

1.  Use la [**función OpenSCManager para**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) obtener un identificador para la base de datos de SCM en un equipo especificado.
2.  Use la [**función OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) [**o CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obtener un identificador para el objeto de servicio.

Para obtener más información, vea los temas siguientes:

-   [Instalación, eliminación y enumeración de servicios](service-installation-removal-and-enumeration.md)
-   [Configuración de servicio](service-configuration.md)
-   [Configuración de un servicio mediante SC](configuring-a-service-using-sc.md)

 

 



