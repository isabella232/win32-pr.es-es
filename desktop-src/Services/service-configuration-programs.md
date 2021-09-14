---
description: Los programadores y administradores del sistema usan programas de configuración de servicio para modificar o consultar la base de datos de los servicios instalados.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programas de configuración de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168901"
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

 

 



