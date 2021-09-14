---
description: El SCM mantiene una base de datos de servicios instalados en el Registro.
ms.assetid: 70f24e15-2607-4c32-9192-a9413b74558b
title: Base de datos de servicios instalados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24a92712d6713e2ca31dbc4b768e3b7c2983ffc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265063"
---
# <a name="database-of-installed-services"></a>Base de datos de servicios instalados

El SCM mantiene una base de datos de servicios instalados en el Registro. El SCM y los programas que agregan, modifican o configuran servicios usan la base de datos. La siguiente es la clave del Registro para esta base de datos: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services**.

Esta clave contiene una subclave para cada servicio instalado y servicio de controlador. El nombre de la subclave es el nombre del servicio, tal y como especifica la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) cuando un programa de configuración de servicio instaló el servicio.

Cuando se instala el sistema, se crea una copia inicial de la base de datos. La base de datos contiene entradas para los controladores de dispositivo necesarios durante el arranque del sistema. La base de datos incluye la siguiente información sobre cada servicio instalado y servicio de controlador:

-   El tipo de servicio. Esto indica si el servicio se ejecuta en su propio proceso o comparte un proceso con otros servicios. Para los servicios de controlador, esto indica si el servicio es un controlador de kernel o un controlador del sistema de archivos.
-   Tipo de inicio. Esto indica si el servicio o el servicio de controlador se inicia automáticamente al iniciar el sistema (servicio de inicio automático) o si el SCM lo inicia cuando lo solicita un programa de control de servicios (servicio de inicio a petición). El tipo de inicio también puede indicar que el servicio o el servicio de controlador está deshabilitado, en cuyo caso no se puede iniciar.
-   Nivel de control de error. Esto especifica la gravedad del error si el servicio o el servicio de controlador no se inicia durante el inicio del sistema y determina la acción que realizará el programa de inicio.
-   Ruta de acceso completa del archivo ejecutable. La extensión de nombre de archivo .EXE para los servicios y .SYS para los servicios de controlador.
-   Información de dependencia opcional que se usa para determinar el orden adecuado para iniciar servicios o servicios de controlador. Para los servicios, esta información puede incluir una lista de servicios que el SCM debe iniciar para poder iniciar el servicio especificado, el nombre de un grupo de pedidos de carga del que forma parte el servicio y un identificador de etiqueta que indica el orden de inicio del servicio en su grupo de ordenación de carga. Para los servicios de controlador, esta información incluye una lista de controladores que deben iniciarse antes del controlador especificado.
-   Para los servicios, un nombre de cuenta y una contraseña opcionales. El programa de servicio se ejecuta en el contexto de esta cuenta. Si no se especifica ninguna cuenta, el servicio se ejecuta en el contexto de la [cuenta LocalSystem](localsystem-account.md).
-   Para los servicios de controlador, un nombre de objeto de controlador opcional (por ejemplo, \\ FileSystem Rdr o \\ Driver \\ Xns), que usa el sistema de \\ E/S para cargar el controlador de dispositivo. Si no se especifica ningún nombre, el sistema de E/S crea un nombre predeterminado basado en el nombre del servicio de controlador.

> [!Note]  
> Esta base de datos también se conoce como la base de datos ServicesActive o la base de datos SCM. Debe usar las funciones proporcionadas por el SCM, en lugar de modificar la base de datos directamente.

 

 

 



