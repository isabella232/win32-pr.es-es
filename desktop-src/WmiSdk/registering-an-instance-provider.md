---
description: Para crear un proveedor de instancias WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ InstanceProviderRegistration.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Registrar un proveedor de instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544694"
---
# <a name="registering-an-instance-provider"></a>Registrar un proveedor de instancias

Para crear un [*proveedor de instancias*](gloss-i.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI. En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).

En el procedimiento siguiente se describe cómo registrar un proveedor de instancias.

**Para registrar un proveedor de instancias**

1.  Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor.
2.  Cree una instancia de la clase [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) que describa el conjunto de características del proveedor.

    La clase [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , que proporciona valores booleanos que indican la compatibilidad con características concretas y una matriz de cadenas para indicar la compatibilidad con consultas.

    Asegúrese de etiquetar la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y [**dinámicos**](standard-wmi-qualifiers.md) . El calificador indica que WMI debe utilizar un proveedor **dinámico** para recuperar las instancias de clase. El calificador de **proveedor** especifica el nombre del proveedor que debe usar WMI.

En el ejemplo de código siguiente se describe cómo registrar una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



