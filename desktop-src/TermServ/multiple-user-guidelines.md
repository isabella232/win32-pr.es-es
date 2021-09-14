---
title: Directrices para varios usuarios
description: Directrices para desarrollar aplicaciones para varios usuarios en un entorno Servicios de Escritorio remoto usuario.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968003"
---
# <a name="multiple-user-guidelines"></a>Directrices para varios usuarios

En las secciones siguientes se proporcionan instrucciones para desarrollar aplicaciones para varios usuarios en Servicios de Escritorio remoto entorno.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Configuración de la aplicación](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

La instalación de una aplicación para un solo usuario puede crear problemas en un entorno multiusuario Servicios de Escritorio remoto usuario.

</dd> <dt>

[Almacenamiento de información específica del usuario](storing-user-specific-information.md)
</dt> <dd>

Las aplicaciones deben almacenar información específica del usuario en ubicaciones específicas del usuario, aparte de la información global que se aplica a todos los usuarios.

</dd> <dt>

[Espacios de nombres de objeto kernel](kernel-object-namespaces.md)
</dt> <dd>

Servicios de Escritorio remoto varios espacios de nombres para los objetos de kernel; un espacio de nombres global lo usan principalmente los servicios en aplicaciones cliente/servidor.

</dd> <dt>

[Direcciones IP y nombres de equipo](ip-addresses-and-computer-names.md)
</dt> <dd>

No es seguro suponer que el nombre del equipo o la dirección IP que se asignen al equipo se asocian a un único usuario, dado que varios usuarios pueden iniciar sesión a la vez en un servidor host de sesión de Escritorio remoto.

</dd> </dl>

Como siempre, bloquee archivos y bases de datos mientras realiza cambios para evitar la pérdida involuntaria de datos.

La aplicación no debe bloquear los archivos de aplicación en tiempo de ejecución que no sean archivos por usuario. Los archivos en tiempo de ejecución bloqueados pueden evitar que se ejecuten varias instancias de la aplicación o procesos de la aplicación, como los asistentes. Una buena manera de probar qué archivos son archivos de aplicación en tiempo de ejecución es realizar un seguimiento de los archivos que instala el programa de instalación de la aplicación. Los archivos por usuario rara vez se instalan mediante el programa de instalación; por lo tanto, la mayoría de los archivos instalados por el programa de instalación son archivos de aplicación en tiempo de ejecución.

 

 




