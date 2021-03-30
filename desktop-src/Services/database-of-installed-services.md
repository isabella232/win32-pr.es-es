---
description: El SCM mantiene una base de datos de servicios instalados en el registro.
ms.assetid: 70f24e15-2607-4c32-9192-a9413b74558b
title: Base de datos de servicios instalados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24a92712d6713e2ca31dbc4b768e3b7c2983ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002657"
---
# <a name="database-of-installed-services"></a>Base de datos de servicios instalados

El SCM mantiene una base de datos de servicios instalados en el registro. El SCM y los programas que agregan, modifican o configuran los servicios utilizan la base de datos. A continuación se encuentra la clave del registro para esta base de datos: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**.

Esta clave contiene una subclave para cada servicio instalado y servicio de controlador. El nombre de la subclave es el nombre del servicio, tal y como lo especifica la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) cuando un programa de configuración de servicio instala el servicio.

Cuando se instala el sistema, se crea una copia inicial de la base de datos. La base de datos contiene entradas para los controladores de dispositivo necesarios durante el arranque del sistema. La base de datos incluye la siguiente información acerca de cada servicio instalado y servicio de controlador:

-   El tipo de servicio. Indica si el servicio se ejecuta en su propio proceso o comparte un proceso con otros servicios. En el caso de los servicios de controlador, indica si el servicio es un controlador de kernel o un controlador del sistema de archivos.
-   Tipo de inicio. Indica si el servicio o el servicio de controlador se inicia automáticamente al iniciar el sistema (servicio de inicio automático) o si el SCM lo inicia cuando lo solicita un programa de control de servicios (servicio de inicio de petición). El tipo de inicio también puede indicar que el servicio o el servicio de controlador están deshabilitados, en cuyo caso no se puede iniciar.
-   Nivel de control de errores. Esto especifica la gravedad del error si el servicio o el servicio de controlador no se inicia durante el inicio del sistema y determina la acción que realizará el programa de inicio.
-   Ruta de acceso completa del archivo ejecutable. La extensión de nombre de archivo es. EXE para servicios y. SYS para los servicios de controlador.
-   Información de dependencia opcional que se usa para determinar el orden adecuado para iniciar servicios o servicios de controladores. En el caso de los servicios, esta información puede incluir una lista de servicios que el SCM debe iniciar antes de que pueda iniciar el servicio especificado, el nombre de un grupo de orden de carga del que forma parte el servicio y un identificador de etiqueta que indica el orden de inicio del servicio en su grupo de orden de carga. En el caso de los servicios de controlador, esta información incluye una lista de controladores que deben iniciarse antes que el controlador especificado.
-   En el caso de los servicios, un nombre de cuenta y una contraseña opcionales. El programa de servicio se ejecuta en el contexto de esta cuenta. Si no se especifica ninguna cuenta, el servicio se ejecuta en el contexto de la [cuenta LocalSystem](localsystem-account.md).
-   En el caso de los servicios de controlador, es un nombre de objeto de controlador opcional (por ejemplo, sistema de \\ archivos \\ RDR o de \\ controlador \\ XNS) que usa el sistema de e/s para cargar el controlador de dispositivo. Si no se especifica ningún nombre, el sistema de e/s crea un nombre predeterminado basado en el nombre del servicio del controlador.

> [!Note]  
> Esta base de datos también se conoce como la base de datos ServicesActive o la base de datos SCM. Debe utilizar las funciones proporcionadas por el SCM, en lugar de modificar la base de datos directamente.

 

 

 



