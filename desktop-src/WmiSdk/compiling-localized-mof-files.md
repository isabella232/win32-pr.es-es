---
description: Debe compilar el archivo MOF maestro para crear los archivos MOF neutrales y específicos del lenguaje.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Compilación de archivos MOF localizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d23c77fee8a745b6032848c124a24ffb8e7cf626b0ff3c87fecc7e05b14d372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556804"
---
# <a name="compiling-localized-mof-files"></a>Compilación de archivos MOF localizados

Debe compilar el archivo MOF maestro para crear los archivos MOF neutrales y específicos del lenguaje.

Escriba el siguiente comando en un símbolo del sistema para compilar un archivo MOF maestro.

**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS \_ 409 Mastermof.mof**

Al ejecutar este comando, el compilador de MOF crea dos archivos MOF a partir del archivo Mastermof.mof original. El compilador MOF genera una versión independiente del lenguaje, Lnmof.mof, en la que se quitan todos los elementos específicos del lenguaje. También se crea una segunda versión específica del lenguaje, Lsmof.mof. este archivo solo contiene elementos [](qualifier-flavors.md) marcados con el tipo calificador modificado en el archivo Mastermof.mof.

En el ejemplo de código siguiente se muestra el contenido del archivo MOF neutral del lenguaje (Lnmof.mof) que se genera.

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

En el ejemplo de código siguiente se muestra el contenido del archivo MOF específico del lenguaje (Lsmof.mfl) que se genera.

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

La compilación de un archivo MOF con el calificador [**Amended**](qualifier-flavors.md) solo genera archivos MOF independientes independientes que son independientes y específicos del lenguaje. el repositorio CIM no se actualiza con la nueva información de clase. Debe usar el compilador MOF para compilar los dos archivos MOF que la primera compilación produjo antes de que cualquier información de clase esté disponible para WMI.

Al compilar un archivo MOF maestro, solo los calificadores con el tipo [**Amended**](qualifier-flavors.md) se mueven al archivo MOF específico del lenguaje. Los calificadores que no tienen el tipo **Amended** no están localizados y solo existen en la definición de clase básica en el archivo MOF neutral del lenguaje. Los calificadores no localizados se pueden usar para las descripciones predeterminadas si las descripciones localizadas no están disponibles.

Puede usar el [comando de modificación pragma](pragma-amendment.md) en lugar de especificar [**Amended**](qualifier-flavors.md) como un modificador para el compilador MOF. Cualquiera de estas opciones equivale a solicitar versiones específicas del idioma y neutrales del lenguaje de un archivo MOF. Si usa el comando de modificación pragma o la opción de línea de comandos **Amended,** debe especificar el nombre de los archivos de salida mediante las opciones **-MFL** y **-MOF** en el símbolo del sistema.

> [!Note]  
> El archivo MOF neutral del lenguaje que genera el compilador MOF contiene el equivalente decimal del identificador de configuración regional, incluso si este valor se escribió en hexadecimal. En el ejemplo anterior, el compilador ha convertido el valor 0x409 en el número decimal 1033 para el archivo de salida Lnmof.mof.

 

 

 



