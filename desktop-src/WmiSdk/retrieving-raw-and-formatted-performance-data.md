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
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a>Recuperar documentación para objetos de datos de rendimiento sin formato y con formato

En el siguiente tema se describe cómo recuperar la documentación de programación en línea para un objeto de datos con formato o sin formato creado dinámicamente.

WMI contiene una serie de objetos que realizan el seguimiento del rendimiento. Las clases derivadas de [**\_ PerfRawData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contienen datos de rendimiento sin procesar o "sin cocer", y son compatibles con el [proveedor de contador de rendimiento](performance-counter-provider.md). Por el contrario, las clases derivadas de [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contienen datos con formato "cocidos", y son compatibles con el [proveedor de datos de rendimiento con formato](formatted-performance-data-provider.md).

Sin embargo, ambos proveedores admiten una serie de clases secundarias creadas dinámicamente. Dado que las propiedades se agregan en tiempo de ejecución, estas clases pueden contener propiedades no documentadas. Puede usar el código siguiente para identificar qué propiedades tiene una clase creada dinámicamente.

**Para recuperar una descripción de una clase creada dinámicamente**

1.  Cree una instancia del elemento y establezca el calificador corregido en true.

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  Recupere las propiedades de la clase.

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  Mostrar las propiedades.

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

El código siguiente recupera las descripciones de propiedad para el objeto [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) especificado.


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



 

 
