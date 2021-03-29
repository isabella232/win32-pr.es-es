---
title: Uso de TBS
description: Cada comando enviado a TBS está asociado a una entidad específica. Esto se logra mediante la creación de uno o más contextos para una entidad, que después se asocian a cada comando subsiguiente enviado por esa entidad.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- Servicios base de TPM TBS, ejemplos
- Servicios base de TPM TBS, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994277"
---
# <a name="using-tbs"></a>Uso de TBS

La característica servicios base de TPM se divide en cuatro áreas funcionales:

-   [Virtualización de recursos](resource-virtualization.md)
-   [Programación de comandos](command-scheduling.md)
-   [Administración de energía](power-management.md)
-   [Bloqueo de comandos](command-blocking.md)

Para asegurarse de que las distintas entidades no puedan tener acceso a los recursos de los demás, cada comando enviado a TBS está asociado a una entidad específica. Esto se logra mediante la creación de uno o más contextos para una entidad, que después se asocian a cada comando subsiguiente enviado por esa entidad. Cada comando incluye un objeto de contexto, que permite a TBS ejecutar comandos de TPM en el contexto adecuado. Todos los objetos creados por los comandos se vacían desde el TPM cuando se cierra el contexto.

Una entidad crea el contexto antes de obtener acceso por primera vez a TBS y mantiene el contexto hasta que finaliza la realización de los accesos a TBS. Por ejemplo, en el caso de una TSS, la característica de servicios principales de TCG (TCS) de TSS crearía un contexto de TBS cuando se iniciaba y mantener ese contexto activo hasta que se cierre.

En el caso de Windows Server 2008 y Windows Vista, el TBS restringe el acceso a la API de TBS a las cuentas de administrador, NT AUTHORITY \\ LocalService y NT Authority \\ . De forma predeterminada, estas cuentas son las únicas que se pueden conectar a TBS y crear contextos. Las restricciones de acceso se pueden modificar mediante la creación de un **acceso** de clave del registro con **un nombre de** valor de registro de cadena (**reg \_ SZ**). <dl> <dt>

Tipo de datos
</dt> <dd>REG_SZ</dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

Ejemplo:

**O:BAG: BAD: (A;; 0 x00000001;;; BA) (A;; 0 x00000001;;; NS) (A;; 0 x00000001;;; LS**

De forma predeterminada, el número máximo de contextos admitidos por TBS es 25. Este número puede modificarse mediante la creación o modificación de un valor del registro **DWORD** denominado **MaxContexts** en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **TPM**. El uso del contexto de TBS en tiempo real se puede observar mediante la herramienta Monitor de rendimiento para realizar el seguimiento del número de contextos de TBS.

En Windows 8, Windows Server 2012 y versiones posteriores, el TBS permite el acceso a los usuarios estándar y a los administradores. Las claves del registro **SecurityDescriptor** y **MaxContexts** se han quedado obsoletas. En Windows 8, Windows Server 2012 y versiones posteriores, TBS restringe el acceso a determinados comandos mediante el bloqueo de comandos.

Para Windows 10, versión 1607, el TBS permite el acceso desde aplicaciones AppContainer. Para cada versión de TPM, se han agregado las claves **BlockedAppContainerCommands** y **AllowedW8AppContainerCommands** con las listas coincidentes de comandos de TPM bloqueados y permitidos, respectivamente.

En Windows 10, versión 1803, ya no se admiten las claves del registro en **AllowedW8AppContainerCommands** .

 

 




