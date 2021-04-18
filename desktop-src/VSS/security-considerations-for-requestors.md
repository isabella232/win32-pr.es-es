---
description: La infraestructura de VSS requiere que los solicitantes VSS, como las aplicaciones de copia de seguridad, puedan funcionar como clientes COM y como servidor.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Consideraciones de seguridad para los solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360601"
---
# <a name="security-considerations-for-requesters"></a>Consideraciones de seguridad para los solicitantes

La infraestructura de VSS requiere que los solicitantes VSS, como las aplicaciones de copia de seguridad, puedan funcionar como clientes COM y como servidor.

Cuando actúa como un servidor, un solicitante expone un conjunto de interfaces de devolución de llamada COM que se pueden invocar desde procesos externos (como escritores o el servicio VSS). Por lo tanto, los solicitantes necesitan administrar de forma segura qué clientes COM pueden realizar llamadas COM entrantes en su proceso.

Del mismo modo, los solicitantes pueden actuar como cliente COM para las API COM proporcionadas por un VSS Writer o por el servicio VSS. La configuración de seguridad específica del solicitante debe permitir llamadas COM salientes del solicitante a estos otros procesos.

El mecanismo más sencillo para administrar los problemas de seguridad de un solicitante implica la selección correcta de la cuenta de usuario en la que se ejecuta.

Normalmente, los solicitantes deben ejecutarse en un usuario que sea miembro del grupo administradores o del grupo operadores de copia de seguridad, o bien ejecutarse como la cuenta del sistema local.

De forma predeterminada, cuando un solicitante actúa como cliente COM, si no se ejecuta en estas cuentas, cualquier llamada COM se rechaza automáticamente con **E \_ ACCESSDENIED**, sin necesidad de llegar a la implementación del método com.

## <a name="disabling-com-exception-handling"></a>Deshabilitar el control de excepciones COM

Al desarrollar un solicitante, establezca la marca de opciones de COMGLB de donot de la \_ excepción \_ de control de excepciones de com \_ para deshabilitar el control de excepciones com. Es importante hacerlo porque el control de excepciones COM puede enmascarar errores irrecuperables en una aplicación de VSS. El error que se enmascara puede dejar el proceso en un estado inestable e impredecible, lo que puede provocar daños y bloqueos. Para obtener más información acerca de esta marca, vea [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-requester-default-com-access-check-permission"></a>Estableciendo el permiso de comprobación de acceso COM predeterminado del solicitante

Los solicitantes deben tener en cuenta que cuando su proceso actúa como servidor (por ejemplo, permitir que los escritores modifiquen el documento de componentes de copia de seguridad), deben permitir las llamadas entrantes de otros participantes de VSS, como escritores o el servicio VSS.

Sin embargo, de forma predeterminada, un proceso de Windows solo permitirá clientes COM que se ejecuten en la misma sesión de inicio de sesión (el propio SID) o se ejecuten en la cuenta de sistema local. Este es un posible problema porque estos valores predeterminados no son adecuados para la infraestructura de VSS. Por ejemplo, los escritores pueden ejecutarse como una cuenta de usuario de "operador de copia de seguridad" que no está en la misma sesión de inicio de sesión que el proceso solicitante ni una cuenta de sistema local.

Para controlar este tipo de problema, cada proceso de servidor COM puede ejercer un mayor control sobre si un cliente RPC o COM tiene permiso para realizar un método COM implementado por el servidor (un solicitante en este caso) mediante [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer un "permiso de comprobación de acceso com predeterminado" para todo el proceso.

Los solicitantes pueden hacer lo siguiente explícitamente:

-   Permitir el acceso de todos los procesos para llamar al proceso del solicitante.

    Esta opción puede ser adecuada para la mayoría de los solicitantes y se usa en otros servidores COM; por ejemplo, todos los servicios de Windows basados en SVCHOST ya usan esta opción, al igual que todos los servicios COM+ de forma predeterminada.

    Permitir que todos los procesos realicen llamadas COM entrantes no es necesariamente un punto débil de seguridad. Un solicitante que actúa como un servidor COM, al igual que todos los demás servidores COM, conserva siempre la opción de autorizar a sus clientes en cada método COM implementado en su proceso.

    Tenga en cuenta que las devoluciones de llamada COM internas implementadas por VSS están protegidas de forma predeterminada.

    Para permitir que todos los procesos tengan acceso COM a un solicitante, puede pasar un descriptor de seguridad **nulo** como primer parámetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). (Tenga en cuenta que se debe llamar a **CoInitializeSecurity** como máximo una vez para todo el proceso. Consulte la documentación de COM o MSDN para obtener más información sobre las llamadas a **CoInitializeSecurity** ).

    En el ejemplo de código siguiente se muestra cómo un solicitante debe llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) en Windows 8 y windows Server 2012 y versiones posteriores, para que sea compatible con VSS para recursos compartidos de archivos remotos (RVSS):

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Cuando se establece explícitamente la seguridad de nivel COM del solicitante con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), debe hacer lo siguiente:

    -   Establezca el nivel de autenticación en al **menos \_ \_ \_ \_ \_ integridad de nivel** de autenticación de RPC C. Para mejorar la seguridad, considere el uso de la **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C**.
    -   Establezca el nivel de suplantación en la **\_ \_ \_ \_ suplantación de nivel Imp de RPC C**.
    -   Establezca las capacidades de seguridad de ocultación en **EOAC \_ static**. Para obtener más información acerca de la ocultación de la seguridad, consulte [Cloaking](../com/cloaking.md).

    En el ejemplo de código siguiente se muestra cómo un solicitante debe llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) en Windows 7 y windows Server 2008 R2 y versiones anteriores (o en Windows 8 y windows Server 2012 y versiones posteriores, si no es necesaria la compatibilidad con RVSS):

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Cuando se establece explícitamente la seguridad de nivel COM del solicitante con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), debe hacer lo siguiente:

    -   Establezca el nivel de autenticación en al menos el nivel de autenticación de **RPC \_ C \_ \_ \_ Connecta**. Para mejorar la seguridad, considere el uso de la **\_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C**.
    -   Establezca el nivel de suplantación **en \_ \_ nivel IMP \_ \_ de RPC C** , a menos que el proceso del solicitante tenga que permitir la suplantación para llamadas RPC o com específicas que no están relacionadas con VSS.

-   Permitir solo el acceso a los procesos especificados para llamar al proceso del solicitante.

    Un servidor COM (como un solicitante) que llama a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descriptor de seguridad que no **es null** como primer parámetro puede usar el descriptor para configurarlo de modo que acepte las llamadas entrantes solo de los usuarios que pertenecen a un conjunto específico de cuentas.

    Un solicitante debe asegurarse de que los clientes COM que se ejecutan en usuarios válidos estén autorizados para llamar a su proceso. Un solicitante que especifica un descriptor de seguridad en el primer parámetro debe permitir que los siguientes usuarios realicen llamadas entrantes en el proceso del solicitante:

    -   Sistema local
    -   Servicio local

        **Windows XP:** Este valor no se admite hasta Windows Server 2003.

    -   Servicio de red

        **Windows XP:** Este valor no se admite hasta Windows Server 2003.

    -   Miembros del grupo local Administradores
    -   Miembros del grupo operadores de copia de seguridad local
    -   Usuarios especiales que se especifican en la ubicación del Registro siguiente, con "1" como \_ valor de REG DWORD

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a>Controlar explícitamente el acceso de la cuenta de usuario a un solicitante

Hay casos en los que la restricción de acceso a un solicitante a los procesos que se ejecutan como sistema local, o en los grupos de administradores locales o operadores de copia de seguridad locales, puede ser demasiado restrictivo.

Por ejemplo, un proceso de solicitante especificado podría no tener que ejecutarse normalmente en una cuenta de administrador o de operador de copia de seguridad. Por motivos de seguridad, sería mejor no promover artificialmente los privilegios de los procesos para admitir VSS.

En estos casos, se debe modificar la clave del registro **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** para indicar a VSS que un usuario especificado es seguro para ejecutar un solicitante de VSS.

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
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Este mecanismo también se puede usar para restringir explícitamente que un usuario permitido de otro modo no ejecute un solicitante de VSS. En el siguiente ejemplo se restringirá el acceso de la cuenta de administrador de ThatDomain \\ :

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

El administrador de ThatDomain de usuario \\ no podría ejecutar un solicitante de VSS.

## <a name="performing-a-file-backup-of-the-system-state"></a>Realización de una copia de seguridad de archivos del estado del sistema

Si un solicitante realiza una copia de seguridad del estado del sistema mediante la copia de seguridad de archivos individuales en lugar de usar una imagen de volumen para la copia de seguridad, debe llamar a las funciones [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) y [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) para enumerar los vínculos físicos en los archivos que se encuentran en los directorios siguientes:

-   Windows \\ system32 \\ WDI \\ perftrack\\
-   Windows \\ WINSXS\\

Solo los miembros del grupo administradores pueden tener acceso a estos directorios. Por esta razón, este solicitante debe ejecutarse en la cuenta del sistema o en una cuenta de usuario que sea miembro del grupo administradores.

**Windows XP y Windows Server 2003:** Las funciones [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) y [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) no se admiten hasta Windows Vista y Windows Server 2008.

 

 
