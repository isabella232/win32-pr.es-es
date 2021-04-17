---
description: Un proveedor de asociaciones proporciona un mecanismo para registrar perfiles y asociarlos a perfiles que se implementan en distintos espacios de nombres.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Escribir un proveedor de Asociación para la interoperabilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f38f09a5c5771fe7fd04909f8247834b646ad1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105718585"
---
# <a name="writing-an-association-provider-for-interop"></a>Escribir un proveedor de Asociación para la interoperabilidad

Un proveedor de asociaciones proporciona un mecanismo para registrar perfiles y asociarlos a perfiles que se implementan en distintos espacios de nombres.

Los proveedores de asociación se utilizan para exponer perfiles estándar, como un perfil de energía. Para ello, se escribe un proveedor de asociación en el espacio de nombres de la raíz o la interoperabilidad que expone las instancias de asociación implementando una clase, que se deriva de [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)). El proveedor se debe registrar tanto en la raíz como en la interoperabilidad, y en el espacio de nombres/raíz <implemented> para admitir el cruce seguro del espacio de nombres cruzado.

Instrumental de administración de Windows (WMI) carga el proveedor de asociación siempre que se ejecute una consulta de asociación en el espacio de nombres de la raíz o la interoperabilidad.

**Para implementar un proveedor de Asociación para la interoperabilidad**

1.  Derive una clase de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) y cree una instancia estática de esta clase derivada en el \\ espacio de nombres de interoperabilidad raíz. Como mínimo, las siguientes propiedades deben propagarse con valores válidos:

    -   [**ID**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredName**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    Aunque [**InstanceID**](/previous-versions//ee309375(v=vs.85)) define de forma única la instancia de **\_ RegisteredProfile de CIM**, la combinación de **RegisteredName**, **RegisteredOrganization** y **RegisteredVersion** debe identificar de forma única el perfil registrado dentro del ámbito de la organización. Para obtener más información acerca de las propiedades individuales, consulte [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

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
    > En el caso de los clientes de Windows, la propiedad **RegisteredOrganization** debe establecerse en 1 y la propiedad **OtherRegisteredOrganization** establecida en "Microsoft".

     

2.  Cree un proveedor que devuelva instancias de Asociación de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile). Se trata de un proceso de dos pasos.

    1.  Cree una clase que se derive de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en los espacios de nombres de interoperabilidad e implementación. Dado que los distintos proveedores pueden implementar el mismo perfil, el nombre de la clase debe ser único. La Convención de nomenclatura recomendada es " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ". Tanto la propiedad **ConformantStandard** como la propiedad **ManagedElement** deben especificar el calificador **msft \_ targetNamespace** que contiene el espacio de nombres al que pertenece esta clase.

        En el ejemplo de código siguiente se describe la sintaxis para derivar la \_ clase Microsoft Process \_ ElementConformsToProfile \_ v1 de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en el \\ espacio de nombres de interoperabilidad raíz. En este ejemplo, el \_ elemento administrado por el proceso de Win32 hace referencia al \\ espacio de nombres root cimv2 mediante el calificador de **msft \_ targetNamespace** .

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        En el ejemplo de código siguiente se describe la sintaxis para derivar la \_ clase Microsoft Process \_ ElementConformsToProfile \_ v1 de [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en el \\ espacio de nombres root cimv2. En este ejemplo, el estándar compatible con [**\_ RegisteredProfile de CIM**](/previous-versions//ee309375(v=vs.85)) hace referencia al \\ espacio de nombres de interoperabilidad raíz mediante el calificador de **msft \_ targetNamespace** .

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Si no se especifica el calificador de **msft \_ targetNamespace** en la propiedad que hace referencia al espacio de nombres implementado, el filtro **ResultClass** de la instrucción "ASSOCIATORS of" no funcionará. Por ejemplo, si no se especifica el calificador de **msft \_ targetNamespace** , la siguiente línea de comandos de Windows PowerShell no devolverá un objeto: **Get-WMIObject-Query "associatorsrs de {ProcessProfile. InstanceId = ' Process '} donde ResultClass = ' \_ proceso Win32 '"**.

        El calificador de **msft \_ targetNamespace** no puede apuntar a un espacio de nombres de un equipo remoto. Por ejemplo, no se admite el siguiente espacio de nombres: msft \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ \\ \\ interoperabilidad de raíz).

    2.  Escriba un proveedor que devuelva instancias de la clase derivada creada. Para obtener más información, consulte [escribir un proveedor de instancias](writing-an-instance-provider.md). Al acceder a las instancias entre espacios de nombres, es posible que tenga que tener acceso a los niveles de seguridad del cliente. Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).

        El proveedor de asociación debe implementar los métodos [**IWbemServices. CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) y [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) . La implementación del método [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) es opcional. Dado que se puede tener acceso a este proveedor desde la \\ interoperabilidad raíz y los \\ <implemented> espacios de nombres raíz, no debe haber una dependencia explícita en un espacio de nombres dentro del proveedor.

3.  Registre el proveedor de asociación en la \\ interoperabilidad raíz y en los \\ <implemented> espacios de nombres raíz. Para obtener más información, vea [registrar un proveedor de instancias](registering-an-instance-provider.md).

    En el ejemplo de código siguiente se describe la sintaxis para registrar el proveedor de asociación en el \\ espacio de nombres de interoperabilidad raíz.

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

    En el ejemplo de código siguiente se describe la sintaxis para registrar el proveedor de asociación en el \\ espacio de nombres root cimv2.

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

4.  Coloque el esquema del [**\_ ElementConformsToProfile de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) en el espacio de nombres implementado. En el caso de los clientes de Windows, este es el archivo Interop. mof que se encuentra en la carpeta% SystemRoot% \\ system32 \\ WBEM.
5.  Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor. El método [**tializeIWbemProviderInit.Ini**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) debe implementarse de forma que permita que se llame para dos espacios de nombres diferentes. Para obtener más información, vea [inicializar un proveedor](initializing-a-provider.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Escribir un proveedor de instancias](writing-an-instance-provider.md)
</dt> <dt>

[Registrar un proveedor de instancias](registering-an-instance-provider.md)
</dt> </dl>

 

 
