---
description: Un proveedor de asociaciones proporciona un mecanismo para registrar perfiles y asociarlos a perfiles que se implementan en espacios de nombres diferentes.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Escribir un proveedor de asociación para interoperabilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d45ceebf9f3465bf9485f4105d9ea2e4438a25c9d169193a8b68c19669b51b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794275"
---
# <a name="writing-an-association-provider-for-interop"></a>Escribir un proveedor de asociación para interoperabilidad

Un proveedor de asociaciones proporciona un mecanismo para registrar perfiles y asociarlos a perfiles que se implementan en espacios de nombres diferentes.

Los proveedores de asociaciones se usan para exponer perfiles estándar, como un perfil de energía. Esto se logra mediante la escritura de un proveedor de asociación en el espacio de nombres raíz/interoperabilidad que expone instancias de asociación mediante la implementación de una clase , que se deriva de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)). El proveedor debe estar registrado tanto en la raíz o interoperabilidad como en el espacio de nombres root/para admitir el recorrido <implemented> entre espacios de nombres.

Windows Instrumental de administración (WMI) carga el proveedor de asociación cada vez que se ejecuta una consulta de asociación en el espacio de nombres raíz o de interoperabilidad.

**Para implementar un proveedor de asociación para la interoperabilidad**

1.  Derive una clase de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) y cree una instancia estática de esta clase derivada en el espacio de nombres \\ de interoperabilidad raíz. Como mínimo, se deben propagar las siguientes propiedades con valores válidos:

    -   [**InstanceID**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredName**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    Aunque [**InstanceID**](/previous-versions//ee309375(v=vs.85)) define de forma única la instancia de **CIM \_ RegisteredProfile**, la combinación de **RegisteredName**, **RegisteredOrganization** y **RegisteredVersion** debe identificar de forma única el perfil registrado dentro del ámbito de la organización. Para obtener más información sobre las propiedades individuales, vea [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

    En el ejemplo de código siguiente se describe la sintaxis para derivar la clase **ProcessProfile** de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) y rellenar la instancia estática.

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > Para Windows, la **propiedad RegisteredOrganization** debe establecerse en 1 y la **propiedad OtherRegisteredOrganization** establecida en "Microsoft".

     

2.  Cree un proveedor que devuelva instancias de asociación [**del elemento \_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile). Se trata de un proceso de dos pasos.

    1.  Cree una clase que se derive del elemento [**\_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en los espacios de nombres de interoperabilidad e implementación. Dado que diferentes proveedores pueden implementar el mismo perfil, el nombre de la clase debe ser único. La convención de nomenclatura recomendada es " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ". La propiedad **ConformantStandard** o **ManagedElement** debe especificar el calificador **\_ TARGETNamespace** de MSFT que contiene el espacio de nombres al que pertenece esta clase.

        En el ejemplo de código siguiente se describe la sintaxis para derivar la clase Microsoft \_ Process \_ ElementConformsToProfile v1 del elemento \_ [**\_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en el espacio de nombres de \\ interoperabilidad raíz. En este ejemplo, el elemento administrado Proceso de Win32 hace referencia al espacio de nombres cimv2 raíz mediante el \_ \\ calificador **\_ TargetNamespace de MSFT.**

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        En el ejemplo de código siguiente se describe la sintaxis para derivar la clase Microsoft \_ Process \_ ElementConformsToProfile v1 del elemento \_ [**\_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en el espacio de nombres \\ cimv2 raíz. En este ejemplo, el estándar [**conforme a CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) hace referencia al espacio de nombres de interoperabilidad \\ raíz mediante el calificador **\_ TargetNamespace de MSFT.**

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Si no se especifica el calificador **\_ TARGETNamespace** de MSFT en la propiedad que hace referencia al espacio de nombres implementado, el filtro **ResultClass** de la instrucción "Associators of" no funcionará. Por ejemplo, si no se especifica el calificador **\_ TARGETNamespace de MSFT,** la siguiente línea de comandos de Windows PowerShell no devolverá un objeto: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32 \_ Process'".**

        El **calificador \_ TargetNamespace de MSFT** no puede apuntar a un espacio de nombres en un equipo remoto. Por ejemplo, no se admite el siguiente espacio de nombres: MSFT \_ TargetNamespace(interoperabilidad \\ \\ \\ \\ <RemoteMachine> \\ \\ \\ \\ raíz).

    2.  Escriba un proveedor que devuelva instancias de la clase derivada creada. Para obtener más información, vea [Escribir un proveedor de instancias.](writing-an-instance-provider.md) Al acceder a instancias entre espacios de nombres, es posible que tenga que acceder a los niveles de seguridad del cliente. Para obtener más información, [vea Suplantar un cliente.](impersonating-a-client.md)

        El proveedor de asociación debe implementar los [**métodos IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) [**e IWbemServices.GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) La implementación del [**IWbemServices.Exemétodo cQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) es opcional. Dado que se puede acceder a este proveedor desde la interoperabilidad raíz y los espacios de nombres raíz, no debe haber una dependencia explícita en un espacio de nombres \\ \\ <implemented> dentro del proveedor.

3.  Registre el proveedor de asociación en la \\ interoperabilidad raíz y en los espacios \\ <implemented> de nombres raíz. Para obtener más información, vea [Registrar un proveedor de instancias.](registering-an-instance-provider.md)

    En el ejemplo de código siguiente se describe la sintaxis para registrar el proveedor de asociación en el espacio de \\ nombres de interoperabilidad raíz.

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    En el ejemplo de código siguiente se describe la sintaxis para registrar el proveedor de asociación en el espacio de \\ nombres cimv2 raíz.

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  Coloque el esquema del elemento [**\_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en el espacio de nombres implementado. Para Windows clientes, este es el archivo interop.mof que se encuentra en la carpeta %systemroot% \\ system32 \\ wbem.
5.  Implemente [**la interfaz IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    WMI usa [**IWbemProviderInit para**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) cargar e inicializar un proveedor. El [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) debe implementarse de forma que se pueda llamar a él para dos espacios de nombres diferentes. Para obtener más información, vea [Inicializar un proveedor.](initializing-a-provider.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Elemento \_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Escribir un proveedor de instancias](writing-an-instance-provider.md)
</dt> <dt>

[Registro de un proveedor de instancias](registering-an-instance-provider.md)
</dt> </dl>

 

 
