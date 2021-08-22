---
description: La infraestructura de VSS requiere que los solicitantes de VSS, como las aplicaciones de copia de seguridad, puedan funcionar como clientes COM y como servidor.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Consideraciones de seguridad para los solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d64a5c817a8c45951d56d3fa12e78a03d8bee9dd742f67755f949d1f90a0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590956"
---
# <a name="security-considerations-for-requesters"></a>Consideraciones de seguridad para los solicitantes

La infraestructura de VSS requiere que los solicitantes de VSS, como las aplicaciones de copia de seguridad, puedan funcionar como clientes COM y como servidor.

Al actuar como servidor, un solicitante expone un conjunto de interfaces de devolución de llamada COM que se pueden invocar desde procesos externos (como escritores o el servicio VSS). Por lo tanto, los solicitantes deben administrar de forma segura qué clientes COM pueden realizar llamadas COM entrantes en su proceso.

Del mismo modo, los solicitantes pueden actuar como un cliente COM para las API COM proporcionadas por vss writer o por el servicio VSS. La configuración de seguridad específica del solicitante debe permitir llamadas COM salientes desde el solicitante a estos otros procesos.

El mecanismo más sencillo para administrar los problemas de seguridad de un solicitante implica la selección adecuada de la cuenta de usuario con la que se ejecuta.

Normalmente, un solicitante debe ejecutarse en un usuario que sea miembro del grupo Administradores o del grupo Operadores de copia de seguridad, o ejecutarse como la cuenta del sistema local.

De forma predeterminada, cuando un solicitante actúa como cliente COM, si no se ejecuta en estas cuentas, cualquier llamada COM se rechaza automáticamente con **E \_ ACCESSDENIED**, sin llegar incluso a la implementación del método COM.

## <a name="disabling-com-exception-handling"></a>Deshabilitar el control de excepciones COM

Al desarrollar un solicitante, establezca la marca de opciones globales COM COMGLB EXCEPTION DONOT HANDLE para deshabilitar el control \_ \_ de \_ excepciones COM. Es importante hacerlo porque el control de excepciones COM puede enmascarar errores irreales en una aplicación VSS. El error enmascarado puede dejar el proceso en un estado inestable e imprevisible, lo que puede provocar daños y errores. Para obtener más información sobre esta marca, vea [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-requester-default-com-access-check-permission"></a>Establecer el permiso de comprobación de acceso COM predeterminado del solicitante

Los solicitantes deben tener en cuenta que cuando su proceso actúa como servidor (por ejemplo, permitiendo a los escritores modificar el documento de componentes de copia de seguridad), deben permitir llamadas entrantes de otros participantes de VSS, como escritores o el servicio VSS.

Sin embargo, de forma predeterminada, un proceso de Windows solo permitirá clientes COM que se ejecutan en la misma sesión de inicio de sesión (el SID SELF) o que se ejecutan en la cuenta del sistema local. Se trata de un posible problema porque estos valores predeterminados no son adecuados para la infraestructura de VSS. Por ejemplo, los escritores pueden ejecutarse como una cuenta de usuario "Operador de copia de seguridad" que no está en la misma sesión de inicio de sesión que el proceso del solicitante ni una cuenta de sistema local.

Para controlar este tipo de problema, cada proceso de servidor COM puede ejercer un mayor control sobre si un cliente RPC o COM puede realizar un método COM implementado por el servidor (un solicitante en este caso) mediante [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer un "permiso de comprobación de acceso COM predeterminado" para todo el proceso.

Los solicitantes pueden hacer explícitamente lo siguiente:

-   Permitir que todos los procesos accedan a la llamada al proceso del solicitante.

    Esta opción puede ser adecuada para la gran mayoría de los solicitantes y la usan otros servidores COM, por ejemplo, todos los servicios Windows basados en SVCHOST ya usan esta opción, al igual que todos los servicios COM+ de forma predeterminada.

    Permitir que todos los procesos realicen llamadas COM entrantes no es necesariamente un punto débil de seguridad. Un solicitante que actúa como servidor COM, al igual que todos los demás servidores COM, siempre conserva la opción de autorizar a sus clientes en todos los métodos COM implementados en su proceso.

    Tenga en cuenta que las devoluciones de llamada COM internas implementadas por VSS están protegidas de forma predeterminada.

    Para permitir el acceso COM de todos los procesos a un solicitante, puede pasar un descriptor de seguridad **NULL** como primer parámetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). (Tenga en cuenta que se debe llamar a **CoInitializeSecurity** como máximo una vez durante todo el proceso. Consulte la documentación COM o MSDN para obtener más información sobre **las llamadas a CoInitializeSecurity).**

    En el ejemplo de código siguiente se muestra cómo un solicitante debe llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) en Windows 8 y Windows Server 2012 y versiones posteriores, con el fin de ser compatible con VSS para recursos compartidos de archivos remotos (RVSS):

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

    Al establecer explícitamente la seguridad de nivel COM de un solicitante [**con CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)debe hacer lo siguiente:

    -   Establezca el nivel de autenticación en al menos **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY**. Para mejorar la seguridad, considere la posibilidad de usar **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**.
    -   Establezca el nivel de suplantación en **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE**.
    -   Establezca las funcionalidades de seguridad de protección **en EOAC \_ STATIC**. Para obtener más información sobre la protección de la seguridad, vea [La protección de](../com/cloaking.md).

    En el ejemplo de código siguiente se muestra cómo un solicitante debe llamar a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) en Windows 7 y Windows Server 2008 R2 y versiones anteriores (o en Windows 8 y Windows Server 2012 y versiones posteriores, si no se necesita compatibilidad con DHCPSS):

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

    Al establecer explícitamente la seguridad de nivel COM de un solicitante [**con CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)debe hacer lo siguiente:

    -   Establezca el nivel de autenticación en al menos **RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT**. Para mejorar la seguridad, considere la posibilidad de usar **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**.
    -   Establezca el nivel de suplantación en **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY** a menos que el proceso del solicitante necesite permitir la suplantación para llamadas RPC o COM específicas que no están relacionadas con VSS.

-   Permitir solo el acceso a los procesos especificados para llamar al proceso del solicitante.

    Un servidor COM (por ejemplo, un solicitante) que llama a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descriptor de seguridad que no sea **NULL** como primer parámetro puede usar el descriptor para configurarse para aceptar llamadas entrantes solo de usuarios que pertenecen a un conjunto específico de cuentas.

    Un solicitante debe asegurarse de que los clientes COM que se ejecutan en usuarios válidos están autorizados para llamar a su proceso. Un solicitante que especifica un descriptor de seguridad en el primer parámetro debe permitir que los siguientes usuarios realicen llamadas entrantes en el proceso del solicitante:

    -   Sistema local
    -   Servicio local

        **Windows XP:** Este valor no se admite hasta Windows Server 2003.

    -   Servicio de red

        **Windows XP:** Este valor no se admite hasta Windows Server 2003.

    -   Miembros del grupo administradores local
    -   Miembros del grupo operadores de copia de seguridad local
    -   Usuarios especiales que se especifican en la ubicación del Registro siguiente, con "1" como valor \_ REG DWORD

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a>Controlar explícitamente el acceso de la cuenta de usuario a un solicitante

Hay casos en los que restringir el acceso a un solicitante a procesos que se ejecutan como sistema local, o en los grupos administradores locales o operadores de copia de seguridad locales, puede ser demasiado restrictivo.

Por ejemplo, es posible que un proceso de solicitante especificado no tenga que ejecutarse normalmente con una cuenta de administrador o de operador de copia de seguridad. Por motivos de seguridad, sería mejor no promover artificialmente los privilegios de los procesos para admitir VSS.

En estos casos, la clave del Registro **\_ \_** \\  \\  \\  \\ **VSS** \\ **vssAccessControl** de HKEY LOCAL MACHINE SYSTEM CurrentControlSet Services debe modificarse para indicar a VSS que un usuario especificado es seguro para ejecutar un solicitante de VSS.

En esta clave, debe crear una subclave que tenga el mismo nombre que la cuenta a la que se va a conceder o denegar el acceso. Esta subclave debe establecerse en uno de los valores de la tabla siguiente.

| Value | Significado                                             |
|-------|-----------------------------------------------------|
| 0     | Deniegue el acceso del usuario al escritor y al solicitante.  |
| 1     | Conceda al usuario acceso al escritor.               |
| 2     | Conceda al usuario acceso al solicitante.            |
| 3     | Conceda al usuario acceso al escritor y al solicitante. |



 

En el ejemplo siguiente se concede acceso a la cuenta "MyDomain \\ MyUser":

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

Este mecanismo también se puede usar para restringir explícitamente a un usuario permitido de otro modo la ejecución de un solicitante de VSS. En el ejemplo siguiente se restringirá el acceso desde la cuenta "ThatDomain \\ Administrator":

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

El usuario ThatDomain \\ Administrator no podría ejecutar un solicitante de VSS.

## <a name="performing-a-file-backup-of-the-system-state"></a>Realizar una copia de seguridad de archivos del estado del sistema

Si un solicitante realiza una copia de seguridad del estado del sistema mediante la copia de seguridad de archivos individuales en lugar de usar una imagen de volumen para la copia de seguridad, debe llamar a las funciones [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) y [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) para enumerar los vínculos duros en los archivos que se encuentran en los directorios siguientes:

-   \\Windows system32 \\ WDI \\ perftrack\\
-   \\Windows WINSXS\\

Solo los miembros del grupo Administradores pueden acceder a estos directorios. Por este motivo, este solicitante debe ejecutarse en la cuenta del sistema o en una cuenta de usuario que sea miembro del grupo Administradores.

**Windows XP y Windows Server 2003:** Las [**funciones FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) y [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) no se admiten hasta Windows Vista y Windows Server 2008.

 

 
