---
description: Los programadores y administradores del sistema utilizan programas de configuración de servicio para modificar o consultar la base de datos de servicios instalados.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programas de configuración de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154136"
---
# <a name="service-configuration-programs"></a>Programas de configuración de servicio

Los programadores y administradores del sistema utilizan programas de configuración de servicio para modificar o consultar la base de datos de servicios instalados. También se puede tener acceso a la base de datos mediante las funciones del registro. Sin embargo, solo debe usar las funciones de configuración de SCM, que garantizan que el servicio esté correctamente instalado y configurado.

Las funciones de configuración de SCM requieren un identificador a un objeto SCManager o un identificador a un objeto de servicio. Para obtener estos identificadores, el programa de configuración del servicio debe:

1.  Utilice la función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para obtener un identificador de la base de datos SCM en un equipo especificado.
2.  Utilice la función [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) o [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obtener un identificador para el objeto de servicio.

Para obtener más información, vea los temas siguientes:

-   [Instalación, eliminación y enumeración del servicio](service-installation-removal-and-enumeration.md)
-   [Configuración de servicio](service-configuration.md)
-   [Configuración de un servicio mediante SC](configuring-a-service-using-sc.md)

 

 



