---
title: Uso de TBS
description: Cada comando enviado al TBS está asociado a una entidad específica. Esto se logra mediante la creación de uno o varios contextos para una entidad, que luego se asocian a cada comando posterior enviado por esa entidad.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TPM Base Services TBS , ejemplos
- TPM Base Services TBS , mediante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243759"
---
# <a name="using-tbs"></a>Uso de TBS

La característica Servicios base de TPM se divide en cuatro áreas funcionales:

-   [Virtualización de recursos](resource-virtualization.md)
-   [Programación de comandos](command-scheduling.md)
-   [Administración de energía](power-management.md)
-   [Bloqueo de comandos](command-blocking.md)

Para asegurarse de que las distintas entidades no puedan tener acceso a los recursos del otro, cada comando enviado al TBS está asociado a una entidad específica. Esto se logra mediante la creación de uno o varios contextos para una entidad, que luego se asocian a cada comando posterior enviado por esa entidad. Cada comando incluye un objeto de contexto, que permite a los TB ejecutar comandos tpm en el contexto adecuado. Todos los objetos creados por comandos se vacían del TPM cuando se cierra el contexto.

Una entidad crea el contexto antes de acceder por primera vez al TBS y mantiene el contexto hasta que termina de realizar accesos TBS. Por ejemplo, en el caso de un TSS, la característica TCG Core Services (TCS) del TSS crearía un contexto TBS cuando se inicie y mantendrá ese contexto activo hasta que se cierre.

Para Windows Server 2008 y Windows Vista, TBS restringe el acceso a la API de TBS a las cuentas Administrators, NT AUTHORITY LocalService y \\ NT AUTHORITY \\ NetworkService. De forma predeterminada, estas cuentas son las únicas que pueden conectarse a TBS y crear contextos. Las restricciones de acceso se pueden modificar mediante la creación de una clave del Registro **Access** con una cadena **(REG \_ SZ)** nombre de valor del Registro **SecurityDescriptor** <dl> <dt>

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

**O:BAG:BAD:(A;;0 x00000001;;; BA)(A;;0 x00000001;;; NS)(A;;0 x00000001;;; LS)**

De forma predeterminada, el número máximo de contextos admitidos por TBS es 25. Este número se puede modificar creando o modificando un valor del Registro **DWORD** denominado **MaxContexts** en **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Tpm**. El uso del contexto de TBS en tiempo real se puede observar mediante la herramienta de supervisión de rendimiento para realizar un seguimiento del número de contextos de TBS.

Por Windows 8, Windows Server 2012 y versiones posteriores, el TBS permite el acceso a usuarios y administradores estándar. Las **claves del Registro SecurityDescriptor** y **MaxContexts** quedaron obsoletas. Por Windows 8, Windows Server 2012 y versiones posteriores, TBS restringe el acceso a determinados comandos mediante el bloqueo de comandos.

Por Windows 10, versión 1607, el TBS permite el acceso desde las aplicaciones AppContainer. Para cada versión de TPM, se han agregado las claves **BlockedAppContainerCommands** y **AllowedW8AppContainerCommands** con las listas correspondientes de comandos TPM bloqueados y permitidos, respectivamente.

Por Windows 10, versión 1803, ya no se admiten las claves del Registro en **AllowedW8AppContainerCommands.**

 

 




