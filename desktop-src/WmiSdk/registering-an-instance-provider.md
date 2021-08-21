---
description: Para crear un proveedor de instancias WMI, debe registrar la instancia de Win32Provider que representa al proveedor mediante una instancia \_ \_ de \_ \_ InstanceProviderRegistration.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Registro de un proveedor de instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc97668a41327eabbeab43760703519fa9009c855c25cf77638459050bb5c71d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817083"
---
# <a name="registering-an-instance-provider"></a>Registro de un proveedor de instancias

Para crear un proveedor de [*instancias*](gloss-i.md) WMI, debe registrar la instancia [**\_ \_ de Win32Provider**](--win32provider.md) que representa al proveedor mediante una instancia de [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md). Como objeto COM, el proveedor debe registrarse con el sistema operativo y WMI. En el procedimiento siguiente se da por supuesto que ya ha implementado el proceso de registro como se describe en [Registro de un proveedor.](registering-a-provider.md)

En el procedimiento siguiente se describe cómo registrar un proveedor de instancias.

**Para registrar un proveedor de instancias**

1.  Cree una instancia de la [**\_ \_ clase Win32Provider**](--win32provider.md) que describa el proveedor.
2.  Cree una instancia de la [**\_ \_ clase InstanceProviderRegistration**](--instanceproviderregistration.md) que describa el conjunto de características del proveedor.

    La [**\_ \_ clase InstanceProviderRegistration**](--instanceproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration,**](--objectproviderregistration.md) que proporciona valores booleanos que indican compatibilidad con características concretas y una matriz de cadenas para indicar la compatibilidad con consultas.

    Asegúrese de etiquetar la clase con los calificadores [**Dynamic**](standard-wmi-qualifiers.md) [**y Provider.**](/windows/desktop/api/Provider/nl-provider-provider) El calificador indica que WMI debe usar un **proveedor dinámico** para recuperar las instancias de clase. El **calificador** Provider especifica el nombre del proveedor que WMI debe usar.

En el ejemplo de código siguiente se describe cómo registrar una [**\_ \_ instancia de Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration.**](--instanceproviderregistration.md)

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

 

 



