---
description: La infraestructura de VSS requiere que los procesos de escritura puedan funcionar como clientes COM y como servidores.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Consideraciones de seguridad para escritores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474586"
---
# <a name="security-considerations-for-writers"></a>Consideraciones de seguridad para escritores

La infraestructura de VSS requiere que los procesos de escritura puedan funcionar como clientes COM y como servidores.

Al actuar como servidores, los escritores de VSS exponen interfaces COM (por ejemplo, los controladores de eventos de VSS como [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) y reciben llamadas COM entrantes de procesos VSS (como solicitantes y el servicio VSS) o llamadas RPC de procesos externos a VSS, normalmente cuando estos procesos generan eventos VSS (por ejemplo, cuando un solicitante llama a [**IVssBackupComponents::GatherWriterMetadata).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) Por lo tanto, vss writer debe administrar de forma segura qué clientes COM pueden realizar llamadas COM entrantes en su proceso.

Del mismo modo, los escritores de VSS también pueden actuar como clientes COM, realizando llamadas COM salientes a devoluciones de llamada proporcionadas por la infraestructura de VSS o llamadas RPC a procesos externos a VSS. Estas devoluciones de llamada proporcionadas por una aplicación de copia de seguridad o por el servicio VSS permiten al escritor realizar tareas como actualizar el documento de componentes de copia de seguridad a través de la interfaz [**IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) Por lo tanto, la configuración de seguridad de VSS debe permitir que los escritores realicen llamadas COM salientes a otros procesos de VSS.

El mecanismo más sencillo para administrar problemas de seguridad del escritor implica la selección adecuada de la cuenta de usuario con la que se ejecuta. Normalmente, un escritor debe ejecutarse con un usuario que sea miembro del grupo Administradores o del grupo Operadores de copia de seguridad, o bien debe ejecutarse como la cuenta del sistema local.

De forma predeterminada, cuando un escritor actúa como cliente COM, si no se ejecuta con estas cuentas, cualquier llamada COM que realiza se rechaza automáticamente con **E \_ ACCESSDENIED** sin llegar a la implementación del método COM.

## <a name="disabling-com-exception-handling"></a>Deshabilitar el control de excepciones COM

Al desarrollar un escritor, establezca la marca de opciones globales COM COM COMGLB EXCEPTION DONOT HANDLE para \_ deshabilitar el control de \_ \_ excepciones COM. Es importante hacerlo porque el control de excepciones COM puede enmascarar errores irreales en una aplicación VSS. El error enmascarado puede dejar el proceso en un estado inestable e imprevisible, lo que puede provocar daños y errores. Para obtener más información sobre esta marca, vea [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-writer-default-com-access-check-permission"></a>Establecer el permiso de comprobación de acceso COM predeterminado del escritor

Los escritores deben tener en cuenta que cuando sus procesos actúan como servidor (por ejemplo, para controlar eventos vsS), deben permitir llamadas entrantes de otros participantes de VSS, como solicitantes o el servicio VSS.

Sin embargo, de forma predeterminada, un proceso solo permitirá a los clientes COM que se ejecutan en la misma sesión de inicio de sesión el SID SELF) o que se ejecutan en la cuenta de sistema local. Se trata de un posible problema porque estos valores predeterminados no son suficientes para admitir la infraestructura de VSS. Por ejemplo, los solicitantes pueden ejecutarse como una cuenta de usuario "Operador de copia de seguridad" que no está en la misma sesión de inicio de sesión que el proceso de escritura ni una cuenta de sistema local.

Para controlar este tipo de problema, cada proceso de servidor COM puede ejercer un mayor control sobre si un cliente RPC o COM puede realizar un método COM que el servidor (en este caso, un escritor) implementa mediante [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer un permiso de comprobación de acceso COM predeterminado para todo el proceso.

Los escritores pueden hacer explícitamente lo siguiente:

-   Permitir que todos los procesos accedan a la llamada al proceso de escritura.

    Esta opción puede ser adecuada para muchos escritores y la usan otros servidores COM, por ejemplo, todos los servicios de Windows basados en SVCHOST ya usan esta opción, al igual que todos los servicios COM+ de forma predeterminada.

    Permitir que todos los procesos realicen llamadas COM entrantes no es necesariamente un punto débil de seguridad. Un sistema de escritura que actúa como servidor COM, como todos los demás servidores COM, siempre conserva la opción de autorizar a sus clientes en todos los métodos COM implementados en su proceso.

    Para permitir el acceso COM de todos los procesos a un sistema de escritura, puede pasar un descriptor de seguridad **NULL** como primer parámetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). (Tenga en cuenta que se debe llamar a **CoInitializeSecurity** como máximo una vez durante todo el proceso. Consulte la documentación com para obtener más detalles sobre **CoInitializeSecurity).**

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

    Al establecer explícitamente la seguridad de nivel COM de un escritor [**con CoInitializeSecurity,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)debe hacer lo siguiente:

    -   Establezca el nivel de autenticación en al menos **RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT**.

        Para mejorar la seguridad, considere la posibilidad de usar **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**.

    -   Establezca el nivel de suplantación en **RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY** a menos que el proceso de escritura necesite permitir la suplantación para llamadas RPC o COM específicas que no están relacionadas con VSS.

-   Permitir solo el acceso a los procesos especificados para llamar al proceso de escritura.

    Un servidor COM (por ejemplo, un escritor) que llama a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descriptor de seguridad que no es **NULL** puede usar el descriptor para configurarse para aceptar llamadas entrantes solo de usuarios que pertenecen a un conjunto específico de cuentas.

    Un escritor debe asegurarse de que los clientes COM que se ejecutan con usuarios válidos están autorizados para llamar a su proceso. Un sistema de escritura que especifica un descriptor de seguridad en el primer parámetro debe permitir que los siguientes usuarios realicen llamadas entrantes en el proceso del solicitante:

    -   Sistema local
    -   Miembros del grupo de administradores locales
    -   Miembros del grupo operadores de copia de seguridad local
    -   La cuenta con la que se ejecuta el escritor

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a>Controlar explícitamente el acceso de la cuenta de usuario a un escritor

Hay casos en los que restringir el acceso a un sistema de escritura a procesos que se ejecutan como sistema local, o en los grupos locales administradores o operadores de copia de seguridad locales, puede ser demasiado restrictivo.

Por ejemplo, es posible que un proceso de escritura (quizás un escritor que no es de sistema de terceros) no tenga que ejecutarse normalmente con una cuenta de administrador o de operador de copia de seguridad. Por motivos de seguridad, sería mejor no promover artificialmente los privilegios del proceso para admitir VSS.

En estos casos, la clave del Registro **\_ \_** \\  \\  \\  \\  \\ **VSS vssAccessControl** de HKEY LOCAL MACHINE SYSTEM CurrentControlSet Services debe modificarse para indicar a VSS que un usuario especificado es seguro para ejecutar vss writer.

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
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Este mecanismo también se puede usar para restringir explícitamente a un usuario permitido de otro modo la ejecución de vss writer. En el ejemplo siguiente se restringirá el acceso desde la cuenta "ThatDomain \\ Administrator":

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

El usuario ThatDomain \\ Administrator no podría ejecutar vsS Writer.

 

 
