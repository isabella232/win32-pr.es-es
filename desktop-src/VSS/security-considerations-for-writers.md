---
description: La infraestructura de VSS requiere procesos de escritura para poder funcionar como clientes COM y como servidores.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Consideraciones de seguridad para escritores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696972"
---
# <a name="security-considerations-for-writers"></a>Consideraciones de seguridad para escritores

La infraestructura de VSS requiere procesos de escritura para poder funcionar como clientes COM y como servidores.

Cuando actúan como servidores, los escritores de VSS exponen interfaces COM (por ejemplo, los controladores de eventos de VSS como [**CVssWriter::**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)GatherWriterMetadata) y reciben llamadas com entrantes desde procesos de VSS (como solicitantes y el servicio VSS) o llamadas RPC desde procesos externos a VSS, normalmente cuando estos procesos generan eventos VSS (por ejemplo, cuando un solicitante llama a [**IVssBackupComponents::**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)) Por lo tanto, una VSS Writer necesita administrar de forma segura qué clientes COM pueden realizar llamadas COM entrantes en su proceso.

Del mismo modo, los escritores de VSS también pueden actuar como clientes COM, realizar llamadas COM salientes a devoluciones de llamada proporcionadas por la infraestructura de VSS o llamadas RPC a procesos externos a VSS. Estas devoluciones de llamada que son proporcionadas por una aplicación de copia de seguridad o por el servicio VSS permiten al escritor realizar tareas como la actualización del documento componentes de copia de seguridad a través de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) . Por lo tanto, la configuración de seguridad de VSS debe permitir que los escritores realicen llamadas COM salientes en otros procesos de VSS.

El mecanismo más sencillo para administrar los problemas de seguridad del sistema de escritura implica la selección adecuada de la cuenta de usuario en la que se ejecuta. Normalmente, un sistema de escritura necesita ejecutarse en un usuario que sea miembro del grupo administradores o del grupo operadores de copia de seguridad, o bien debe ejecutarse como la cuenta del sistema local.

De forma predeterminada, cuando un escritor actúa como cliente COM, si no se ejecuta en estas cuentas, cualquier llamada COM que realice se rechazará automáticamente con **E \_ ACCESSDENIED** sin necesidad de llegar a la implementación del método com.

## <a name="disabling-com-exception-handling"></a>Deshabilitar el control de excepciones COM

Al desarrollar un escritor, establezca la marca de COMGLB donot de la \_ excepción \_ \_ de identificador de opciones globales de com para deshabilitar el control de excepciones com. Es importante hacerlo porque el control de excepciones COM puede enmascarar errores irrecuperables en una aplicación de VSS. El error que se enmascara puede dejar el proceso en un estado inestable e impredecible, lo que puede provocar daños y bloqueos. Para obtener más información acerca de esta marca, vea [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-writer-default-com-access-check-permission"></a>Estableciendo el permiso de comprobación de acceso COM predeterminado del escritor

Los escritores deben tener en cuenta que cuando sus procesos actúan como un servidor (por ejemplo, para controlar los eventos de VSS), deben permitir llamadas entrantes de otros participantes de VSS, como solicitantes o el servicio VSS.

Sin embargo, de forma predeterminada, un proceso solo permitirá que los clientes COM que se ejecutan en la misma sesión de inicio de sesión sean el propio SID) o que se ejecuten en la cuenta de sistema local. Este es un posible problema porque estos valores predeterminados no son suficientes para admitir la infraestructura de VSS. Por ejemplo, los solicitantes pueden ejecutarse como una cuenta de usuario de "operador de copia de seguridad" que no sea en la misma sesión de inicio de sesión que el proceso de escritor ni una cuenta de sistema local.

Para controlar este tipo de problema, cada proceso de servidor COM puede ejercer un mayor control sobre si un cliente RPC o COM tiene permiso para realizar un método COM el servidor (un escritor en este caso) implementa mediante [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer un permiso de comprobación de acceso com predeterminado para todo el proceso.

Los escritores pueden hacer lo siguiente explícitamente:

-   Permitir el acceso de todos los procesos para llamar al proceso de escritura.

    Esta opción puede ser adecuada para muchos escritores y se usa en otros servidores COM; por ejemplo, todos los servicios de Windows basados en SVCHOST ya usan esta opción, al igual que todos los servicios COM+ de forma predeterminada.

    Permitir que todos los procesos realicen llamadas COM entrantes no es necesariamente un punto débil de seguridad. Un escritor que actúa como un servidor COM, al igual que todos los demás servidores COM, conserva siempre la opción de autorizar a sus clientes en cada método COM implementado en su proceso.

    Para permitir que todos los procesos tengan acceso COM a un escritor, puede pasar un descriptor de seguridad **nulo** como primer parámetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). (Tenga en cuenta que se debe llamar a **CoInitializeSecurity** como máximo una vez para todo el proceso. Consulte la documentación de COM para obtener más detalles sobre **CoInitializeSecurity**).

    A continuación se muestra un ejemplo de código que incluye una llamada a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    Al establecer explícitamente la seguridad de nivel COM de un escritor con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), debe hacer lo siguiente:

    -   Establezca el nivel de autenticación en al menos el nivel de autenticación de **RPC \_ C \_ \_ \_ Connecta**.

        Para mejorar la seguridad, considere el uso de la **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C**.

    -   Establezca el nivel de suplantación **en \_ \_ nivel IMP \_ \_ de RPC C** , a menos que el proceso del escritor necesite permitir la suplantación para llamadas RPC o com específicas que no están relacionadas con VSS.

-   Permitir solo el acceso a los procesos especificados para llamar al proceso de escritura.

    Un servidor COM (por ejemplo, un escritor) que llama a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descriptor de seguridad que no **es null** puede usar el descriptor para configurarlo para que acepte llamadas entrantes solo de los usuarios que pertenecen a un conjunto específico de cuentas.

    Un escritor debe asegurarse de que los clientes COM que se ejecutan en usuarios válidos estén autorizados para llamar a su proceso. Un escritor que especifica un descriptor de seguridad en el primer parámetro debe permitir que los siguientes usuarios realicen llamadas entrantes en el proceso del solicitante:

    -   Sistema local
    -   Miembros del grupo local Administradores
    -   Miembros del grupo operadores de copia de seguridad local
    -   La cuenta en la que se está ejecutando el escritor

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a>Controlar explícitamente el acceso de la cuenta de usuario a un escritor

Hay casos en los que es necesario restringir el acceso a un sistema de escritura a los procesos que se ejecutan como sistema local, o en los grupos locales de administradores locales o operadores de copia de seguridad locales, que pueden ser demasiado restrictivos.

Por ejemplo, un proceso de escritor (quizás un escritor que no sea del sistema de terceros) podría no tener normalmente que ejecutarse en una cuenta de administrador o de operador de copia de seguridad. Por motivos de seguridad, sería mejor no promover artificialmente los privilegios del proceso para admitir VSS.

En estos casos, se debe modificar la clave del registro **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** para indicar a VSS que un usuario especificado es seguro para ejecutar una VSS Writer.

Bajo esta clave, debe crear una subclave con el mismo nombre que la cuenta a la que se va a conceder o denegar el acceso. Esta subclave debe establecerse en uno de los valores de la tabla siguiente.

| Value | Significado                                             |
|-------|-----------------------------------------------------|
| 0     | Deniegue el acceso del usuario al escritor y al solicitante.  |
| 1     | Conceda al usuario acceso al escritor.               |
| 2     | Conceda al usuario acceso al solicitante.            |
| 3     | Conceda al usuario acceso al escritor y al solicitante. |



 

En el siguiente ejemplo se concede acceso a la cuenta "midominio mi \\ usuario":

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Este mecanismo también se puede usar para restringir explícitamente que un usuario permitido de otro modo no ejecute un VSS Writer. En el siguiente ejemplo se restringirá el acceso de la cuenta de administrador de ThatDomain \\ :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

El administrador de ThatDomain de usuario \\ no podría ejecutar un VSS Writer.

 

 
