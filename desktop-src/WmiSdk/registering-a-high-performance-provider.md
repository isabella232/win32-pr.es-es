---
description: Al igual que otros proveedores de instancias, registra un proveedor de alto rendimiento con Microsoft Windows&\# 160; Instrumental de administración (WMI) mediante la creación de una instancia de las \_ \_ clases Win32Provider \_ \_ e InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrar un proveedor de High-Performance de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063932"
---
# <a name="registering-a-high-performance-provider"></a>Registrar un proveedor de High-Performance de datos

Al igual que otros proveedores de instancias, se registra un proveedor de alto rendimiento con Microsoft Windows Management Instrumentation (WMI) mediante la creación de una instancia de las clases [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration.**](--instanceproviderregistration.md) La **\_ \_ instancia de Win32Provider** define la implementación física del proveedor y la **\_ \_ instancia instanceProviderRegistration** define el conjunto de características del proveedor. Para obtener más información, [vea Registrar un proveedor.](registering-a-provider.md)

En el procedimiento siguiente se describe cómo registrar un proveedor de instancias de alto rendimiento.

**Para registrar un proveedor de instancias de alto rendimiento**

1.  Cree una instancia de la [**\_ \_ clase Win32Provider**](--win32provider.md) que describa el proveedor.

    Asegúrese de agregar una **propiedad ClientLoadableCLSID** a la [**\_ \_ instancia de Win32Provider.**](--win32provider.md) Si el proveedor y el cliente residen en el mismo equipo, WMI carga el proveedor en proceso en el cliente mediante **ClientLoadableCLSID** como identificador de clase. Cuando el proveedor y el cliente residen en equipos diferentes, WMI carga el proveedor en proceso en WMI. WMI también usa **ClientLoadableCLSID para** admitir operaciones de actualización.

2.  Cree una instancia de la [**\_ \_ clase InstanceProviderRegistration**](--instanceproviderregistration.md) que describa el conjunto de características del proveedor.

    Asegúrese de etiquetar la clase con los calificadores [**Dynamic**](dynamic-qualifier.md) [**y Provider.**](/windows/desktop/api/Provider/nl-provider-provider) El **calificador** dinámico indica que WMI debe usar un proveedor para recuperar las instancias de clase. El **calificador** Provider especifica el nombre del proveedor que WMI debe usar.

    Un proveedor de alto rendimiento también debe admitir operaciones, operaciones de enumeración o ambas. Asegúrese de usar las **propiedades SupportsGet** y **SupportsEnumeration** en la implementación.

En el ejemplo de código siguiente se muestra cómo implementar las clases [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) para un proveedor de alto rendimiento.

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Convertir un proveedor de instancias en un High-Performance de recursos](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



