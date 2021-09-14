---
description: En el tema siguiente se describe cómo recuperar la documentación de programación en línea para un objeto de datos sin formato creado dinámicamente.
ms.assetid: B3CD7E2C-9FCF-42FB-8713-01A696E905B0
ms.tgt_platform: multiple
title: Recuperación de documentación para objetos de datos de rendimiento sin formato y sin formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ab9cf66aa4536da25102511fdcbcab6bdd5202
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063912"
---
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a>Recuperación de documentación para objetos de datos de rendimiento sin formato y sin formato

En el tema siguiente se describe cómo recuperar la documentación de programación en línea para un objeto de datos sin formato creado dinámicamente.

WMI contiene una serie de objetos que realiza un seguimiento del rendimiento. Las clases derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contienen datos de rendimiento sin procesar o "nococodados", y son compatibles con el proveedor de contadores [de rendimiento](performance-counter-provider.md). Por el contrario, las clases derivadas de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contienen datos "cociados" o con formato, y son compatibles con el proveedor de datos de rendimiento [con formato](formatted-performance-data-provider.md).

Sin embargo, ambos proveedores admiten una serie de clases secundarias creadas dinámicamente. Dado que las propiedades se agregan en tiempo de ejecución, estas clases pueden contener propiedades no documentadas. Puede usar el código siguiente para identificar qué propiedades tiene una clase creada dinámicamente determinada.

**Para recuperar una descripción de una clase creada dinámicamente**

1.  Cree una instancia del elemento y establezca el calificador modificado en true.

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  Recupere las propiedades de la clase .

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

    

El código siguiente recupera las descripciones de propiedades para el objeto [**\_ PerfFormattedData de Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) especificado.


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



 

 
