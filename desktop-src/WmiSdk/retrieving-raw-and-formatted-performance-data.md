---
description: En el siguiente tema se describe cómo recuperar la documentación de programación en línea para un objeto de datos con formato o sin formato creado dinámicamente.
ms.assetid: B3CD7E2C-9FCF-42FB-8713-01A696E905B0
ms.tgt_platform: multiple
title: Recuperar documentación para objetos de datos de rendimiento sin formato y con formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ab9cf66aa4536da25102511fdcbcab6bdd5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361447"
---
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a><span data-ttu-id="ed289-103">Recuperar documentación para objetos de datos de rendimiento sin formato y con formato</span><span class="sxs-lookup"><span data-stu-id="ed289-103">Retrieving Documentation for Raw and Formatted Performance Data Objects</span></span>

<span data-ttu-id="ed289-104">En el siguiente tema se describe cómo recuperar la documentación de programación en línea para un objeto de datos con formato o sin formato creado dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="ed289-104">The following topic describes how to retrieve the on-line programming documentation for a dynamically-created raw or formatted data object.</span></span>

<span data-ttu-id="ed289-105">WMI contiene una serie de objetos que realizan el seguimiento del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="ed289-105">WMI contains a number of objects that track performance.</span></span> <span data-ttu-id="ed289-106">Las clases derivadas de [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contienen datos de rendimiento sin procesar o "sin cocer", y son compatibles con el [proveedor de contador de rendimiento](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ed289-106">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contain raw, or "uncooked" performance data, and are supported by the [Performance Counter provider](performance-counter-provider.md).</span></span> <span data-ttu-id="ed289-107">Por el contrario, las clases derivadas de [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contienen datos con formato "cocidos", y son compatibles con el [proveedor de datos de rendimiento con formato](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ed289-107">In contrast, classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contain "cooked", or formatted data, and are supported by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="ed289-108">Sin embargo, ambos proveedores admiten una serie de clases secundarias creadas dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="ed289-108">However, both providers support a number of dynamically-created child classes.</span></span> <span data-ttu-id="ed289-109">Dado que las propiedades se agregan en tiempo de ejecución, estas clases pueden contener propiedades no documentadas.</span><span class="sxs-lookup"><span data-stu-id="ed289-109">Because the properties are added at run-time, these classes may contain undocumented properties.</span></span> <span data-ttu-id="ed289-110">Puede usar el código siguiente para identificar qué propiedades tiene una clase creada dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="ed289-110">You can use the following code to identify what properties a given dynamically-created class has.</span></span>

<span data-ttu-id="ed289-111">**Para recuperar una descripción de una clase creada dinámicamente**</span><span class="sxs-lookup"><span data-stu-id="ed289-111">**To retrieve a description of a dynamically-created class**</span></span>

1.  <span data-ttu-id="ed289-112">Cree una instancia del elemento y establezca el calificador corregido en true.</span><span class="sxs-lookup"><span data-stu-id="ed289-112">Create an instance of the item, and set the amended qualifier to true.</span></span>

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  <span data-ttu-id="ed289-113">Recupere las propiedades de la clase.</span><span class="sxs-lookup"><span data-stu-id="ed289-113">Retrieve the properties of the class.</span></span>

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  <span data-ttu-id="ed289-114">Mostrar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed289-114">Display the properties.</span></span>

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

<span data-ttu-id="ed289-115">El código siguiente recupera las descripciones de propiedad para el objeto [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) especificado.</span><span class="sxs-lookup"><span data-stu-id="ed289-115">The following code retrieves the property descriptions for the specified [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) object.</span></span>


```PowerShell
$osClass = New-Object System.Management.ManagementClass Win32_PerfFormattedData_APPPOOLCountersProvider_APPPOOLWAS  
$osClass.Options.UseAmendedQualifiers = $true  
  
# Get the Properties in the class  
$properties = $osClass.Properties  
"This class has {0} properties as follows:" -f $properties.count  
  
  
# display the Property name, description, type, qualifiers and instance values  
  
foreach ($property in $properties) {  
"Property Name: {0}" -f $property.Name  
"Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
"Type:          {0}" -f $property.Type  
"-------"  
}
```



 

 
