---
description: Una matriz es una lista indizada de valores de datos que son del mismo tipo de datos, a los que se puede hacer referencia. Además de las matrices numéricas y de cadena, MOF admite matrices de objetos incrustados y referencias.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Matrices MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275788"
---
# <a name="mof-arrays"></a>Matrices MOF

Una matriz es una lista indizada de valores de datos que son del mismo tipo de datos, a los que se puede hacer referencia. Además de las matrices numéricas y de cadena, MOF admite matrices de objetos incrustados y referencias.

Las siguientes reglas definen una matriz de MOF:

-   Los corchetes usados después del identificador de propiedad especifican una matriz en una definición de clase.

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   Todas las matrices deben ser unidimensionales.
-   Las matrices pueden estar sin enlazar o tener un tamaño explícito.

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    WMI implementa matrices enlazadas y sin enlazar como estructuras **SAFEARRAY** , lo que permite que WMI varíe las dimensiones de la matriz en tiempo de ejecución. Al declarar una matriz con un tamaño explícito, WMI almacena el tamaño como calificador y trata el tamaño como el tamaño máximo sugerido. Sin embargo, WMI puede expandir el tamaño si es necesario. Cambiar el tamaño explícito no tiene ningún efecto en los datos reales.

-   Las matrices se inicializan especificando valores del tipo adecuado en una lista separada por comas.

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   Una matriz de referencias se declara como una matriz de cadenas de ruta de acceso del objeto.

    Al declarar una cadena de ruta de acceso de objeto, no coloque espacios en blanco entre los elementos de la ruta de acceso del objeto. En el ejemplo siguiente se describe cómo declarar una referencia de ruta de acceso de objeto.

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   Puede usar una matriz como parámetro para un método, pero no como un valor devuelto para un parámetro de entrada o de entrada-salida.
-   Todos los elementos de una matriz se crean como valores del mismo tipo.

    Si los elementos de una matriz son del tipo de **objeto** , puede colocar cualquier tipo de objeto en la matriz. Por otro lado, si declara un tipo específico de objeto, WMI solo permite objetos de esa clase o subclase en la matriz. En los ejemplos siguientes se muestran declaraciones de matriz que incluyen el uso del tipo de **objeto** .

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



