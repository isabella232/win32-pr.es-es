---
description: Debe compilar el archivo MOF maestro para crear archivos MOF independientes del idioma y específicos del idioma.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Compilar archivos MOF localizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360952"
---
# <a name="compiling-localized-mof-files"></a>Compilar archivos MOF localizados

Debe compilar el archivo MOF maestro para crear archivos MOF independientes del idioma y específicos del idioma.

Escriba el siguiente comando en un símbolo del sistema para compilar un archivo MOF maestro.

**MOFCOMP-MOF: Lnmof. mof-MFL: Lsmof. MFL-enmienda: MS \_ 409 Mastermof. mof**

Al ejecutar este comando, el compilador MOF crea dos archivos MOF a partir del archivo Mastermof. mof original. El compilador MOF genera una versión independiente del lenguaje, Lnmof. mof, en la que se quitan todos los elementos específicos del lenguaje. También se crea una segunda versión específica del lenguaje, Lsmof. mof. este archivo solo contiene elementos marcados con el tipo de calificador [**corregido**](qualifier-flavors.md) en el archivo Mastermof. mof.

En el ejemplo de código siguiente se muestra el contenido del archivo MOF independiente del lenguaje (Lnmof. mof) que se genera.

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

En el ejemplo de código siguiente se muestra el contenido del archivo MOF específico del idioma (Lsmof. MFL) que se genera.

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

La compilación de un archivo MOF con el calificador [**corregido**](qualifier-flavors.md) solo genera archivos MOF independientes del idioma y específicos del idioma; el repositorio CIM no se actualiza con la nueva información de clase. Debe utilizar el compilador MOF para compilar los dos archivos MOF que la primera compilación generó antes de que cualquier información de clase esté disponible en WMI.

Al compilar un archivo MOF maestro, solo los calificadores con el tipo [**modificado**](qualifier-flavors.md) se mueven al archivo MOF específico del idioma. Los calificadores que no tienen el tipo **modificado** no se localizan y solo existen en la definición de clase básica del archivo MOF independiente del lenguaje. Los calificadores no localizados se pueden usar para las descripciones predeterminadas si las descripciones localizadas no están disponibles.

Puede usar el comando [pragma enmiendas](pragma-amendment.md) en lugar de [**especificar que se haya modificado como**](qualifier-flavors.md) modificador al compilador MOF. Cualquiera de estas opciones es equivalente a solicitar versiones específicas del idioma y del idioma de un archivo MOF. Si usa el comando pragma de modificación o la opción de línea de comandos **modificada** , debe especificar el nombre de los archivos de salida con las opciones **-MFL** y **-MOF** en el símbolo del sistema.

> [!Note]  
> El archivo MOF independiente del lenguaje que genera el compilador MOF contiene el equivalente decimal del ID. de configuración regional, aunque este valor se haya escrito en hexadecimal. En el ejemplo anterior, el compilador ha convertido el valor 0xC0A al número decimal 1033 para el archivo de salida Lnmof. mof.

 

 

 



