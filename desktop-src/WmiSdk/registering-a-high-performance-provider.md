---
description: Al igual que otros proveedores de instancias, registra un proveedor de alto rendimiento con Microsoft Windows&\# 160; Instrumental de administración (WMI) mediante la creación de una instancia de las \_ \_ clases Win32Provider y \_ \_ InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrar un proveedor de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082393"
---
# <a name="registering-a-high-performance-provider"></a><span data-ttu-id="50c4d-103">Registrar un proveedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="50c4d-103">Registering a High-Performance Provider</span></span>

<span data-ttu-id="50c4d-104">Al igual que otros proveedores de instancias, se registra un proveedor de alto rendimiento con Microsoft instrumental de administración de Windows (WMI) mediante la creación de una instancia de las clases [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="50c4d-104">Like other instance providers, you register a high-performance provider with Microsoft Windows Management Instrumentation (WMI) by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes.</span></span> <span data-ttu-id="50c4d-105">La instancia de **\_ \_ Win32Provider** define la implementación física del proveedor y la instancia de **\_ \_ InstanceProviderRegistration** define el conjunto de características del proveedor.</span><span class="sxs-lookup"><span data-stu-id="50c4d-105">The **\_\_Win32Provider** instance defines the provider's physical implementation, and the **\_\_InstanceProviderRegistration** instance defines the provider's feature set.</span></span> <span data-ttu-id="50c4d-106">Para obtener más información, vea [registrar un proveedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="50c4d-106">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="50c4d-107">En el procedimiento siguiente se describe cómo registrar un proveedor de instancias de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="50c4d-107">The following procedure describes how to register a high-performance instance provider.</span></span>

<span data-ttu-id="50c4d-108">**Para registrar un proveedor de instancias de alto rendimiento**</span><span class="sxs-lookup"><span data-stu-id="50c4d-108">**To register a high-performance instance provider**</span></span>

1.  <span data-ttu-id="50c4d-109">Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describe el proveedor.</span><span class="sxs-lookup"><span data-stu-id="50c4d-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class describing the provider.</span></span>

    <span data-ttu-id="50c4d-110">Asegúrese de agregar una propiedad **ClientLoadableCLSID** a la instancia de [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="50c4d-110">Be sure to add a **ClientLoadableCLSID** property to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span> <span data-ttu-id="50c4d-111">Si el proveedor y el cliente residen en el mismo equipo, WMI carga el proveedor en proceso en el cliente utilizando **ClientLoadableCLSID** como identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="50c4d-111">If both the provider and client reside on the same computer, WMI loads the provider in-process to the client using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="50c4d-112">Cuando el proveedor y el cliente residen en equipos diferentes, WMI carga el proveedor en proceso en WMI.</span><span class="sxs-lookup"><span data-stu-id="50c4d-112">When the provider and client reside on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="50c4d-113">WMI también usa **ClientLoadableCLSID** para admitir las operaciones de actualización.</span><span class="sxs-lookup"><span data-stu-id="50c4d-113">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

2.  <span data-ttu-id="50c4d-114">Cree una instancia de la clase [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) que describa el conjunto de características del proveedor.</span><span class="sxs-lookup"><span data-stu-id="50c4d-114">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="50c4d-115">Asegúrese de etiquetar la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y [**dinámicos**](dynamic-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="50c4d-115">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="50c4d-116">El calificador **dinámico** indica que WMI debe utilizar un proveedor para recuperar las instancias de clase.</span><span class="sxs-lookup"><span data-stu-id="50c4d-116">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="50c4d-117">El calificador de **proveedor** especifica el nombre del proveedor que debe usar WMI.</span><span class="sxs-lookup"><span data-stu-id="50c4d-117">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

    <span data-ttu-id="50c4d-118">Un proveedor de alto rendimiento también debe ser compatible con la compatibilidad con operaciones, operaciones de enumeración o ambos.</span><span class="sxs-lookup"><span data-stu-id="50c4d-118">A high-performance provider also needs to state support for operations, enumeration operations, or both.</span></span> <span data-ttu-id="50c4d-119">Asegúrese de usar las propiedades **SupportsGet** y **SupportsEnumeration** en su implementación.</span><span class="sxs-lookup"><span data-stu-id="50c4d-119">Make sure you use the **SupportsGet** and **SupportsEnumeration** properties in your implementation.</span></span>

<span data-ttu-id="50c4d-120">En el ejemplo de código siguiente se muestra cómo implementar las clases [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) para un proveedor de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="50c4d-120">The following code example shows you how to implement the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes for a high-performance provider.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="50c4d-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50c4d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50c4d-122">Crear un proveedor de instancias en un proveedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="50c4d-122">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



