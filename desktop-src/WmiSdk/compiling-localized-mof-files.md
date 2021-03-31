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
# <a name="compiling-localized-mof-files"></a><span data-ttu-id="8886b-103">Compilar archivos MOF localizados</span><span class="sxs-lookup"><span data-stu-id="8886b-103">Compiling Localized MOF Files</span></span>

<span data-ttu-id="8886b-104">Debe compilar el archivo MOF maestro para crear archivos MOF independientes del idioma y específicos del idioma.</span><span class="sxs-lookup"><span data-stu-id="8886b-104">You must compile your master MOF file to create the language-neutral and language-specific MOF files.</span></span>

<span data-ttu-id="8886b-105">Escriba el siguiente comando en un símbolo del sistema para compilar un archivo MOF maestro.</span><span class="sxs-lookup"><span data-stu-id="8886b-105">Type the following command at a command prompt to compile a master MOF file.</span></span>

<span data-ttu-id="8886b-106">**MOFCOMP-MOF: Lnmof. mof-MFL: Lsmof. MFL-enmienda: MS \_ 409 Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="8886b-106">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

<span data-ttu-id="8886b-107">Al ejecutar este comando, el compilador MOF crea dos archivos MOF a partir del archivo Mastermof. mof original.</span><span class="sxs-lookup"><span data-stu-id="8886b-107">When you run this command, the MOF compiler creates two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="8886b-108">El compilador MOF genera una versión independiente del lenguaje, Lnmof. mof, en la que se quitan todos los elementos específicos del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="8886b-108">The MOF compiler produces a language-neutral version, Lnmof.mof, in which all language-specific items are removed.</span></span> <span data-ttu-id="8886b-109">También se crea una segunda versión específica del lenguaje, Lsmof. mof. este archivo solo contiene elementos marcados con el tipo de calificador [**corregido**](qualifier-flavors.md) en el archivo Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="8886b-109">A second, language-specific version, Lsmof.mof, is also created; this file contains only items that were marked with the [**Amended**](qualifier-flavors.md) Qualifier Flavor in the Mastermof.mof file.</span></span>

<span data-ttu-id="8886b-110">En el ejemplo de código siguiente se muestra el contenido del archivo MOF independiente del lenguaje (Lnmof. mof) que se genera.</span><span class="sxs-lookup"><span data-stu-id="8886b-110">The following code example shows the contents of the language-neutral MOF file (Lnmof.mof) that is generated.</span></span>

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

<span data-ttu-id="8886b-111">En el ejemplo de código siguiente se muestra el contenido del archivo MOF específico del idioma (Lsmof. MFL) que se genera.</span><span class="sxs-lookup"><span data-stu-id="8886b-111">The following code example shows the contents of the language-specific MOF file (Lsmof.mfl) that is generated.</span></span>

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

<span data-ttu-id="8886b-112">La compilación de un archivo MOF con el calificador [**corregido**](qualifier-flavors.md) solo genera archivos MOF independientes del idioma y específicos del idioma; el repositorio CIM no se actualiza con la nueva información de clase.</span><span class="sxs-lookup"><span data-stu-id="8886b-112">Compiling a MOF file with the [**Amended**](qualifier-flavors.md) qualifier only generates separate language-neutral and language-specific MOF files; the CIM repository is not updated with the new class information.</span></span> <span data-ttu-id="8886b-113">Debe utilizar el compilador MOF para compilar los dos archivos MOF que la primera compilación generó antes de que cualquier información de clase esté disponible en WMI.</span><span class="sxs-lookup"><span data-stu-id="8886b-113">You must use the MOF compiler to compile the two MOF files that the first compilation produced before any class information is available to WMI.</span></span>

<span data-ttu-id="8886b-114">Al compilar un archivo MOF maestro, solo los calificadores con el tipo [**modificado**](qualifier-flavors.md) se mueven al archivo MOF específico del idioma.</span><span class="sxs-lookup"><span data-stu-id="8886b-114">When you compile a master MOF file, only qualifiers with the [**Amended**](qualifier-flavors.md) flavor are moved to the language-specific MOF file.</span></span> <span data-ttu-id="8886b-115">Los calificadores que no tienen el tipo **modificado** no se localizan y solo existen en la definición de clase básica del archivo MOF independiente del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="8886b-115">Qualifiers that do not have the **Amended** flavor are not localized and only exist in the basic class definition in the language-neutral MOF file.</span></span> <span data-ttu-id="8886b-116">Los calificadores no localizados se pueden usar para las descripciones predeterminadas si las descripciones localizadas no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="8886b-116">Nonlocalized qualifiers can be used for default descriptions if localized descriptions are not available.</span></span>

<span data-ttu-id="8886b-117">Puede usar el comando [pragma enmiendas](pragma-amendment.md) en lugar de [**especificar que se haya modificado como**](qualifier-flavors.md) modificador al compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="8886b-117">You can use the [pragma amendment](pragma-amendment.md) command instead of specifying [**Amended**](qualifier-flavors.md) as a switch to the MOF compiler.</span></span> <span data-ttu-id="8886b-118">Cualquiera de estas opciones es equivalente a solicitar versiones específicas del idioma y del idioma de un archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="8886b-118">Either of these options are equivalent to requesting language-specific and language-neutral versions of a MOF file.</span></span> <span data-ttu-id="8886b-119">Si usa el comando pragma de modificación o la opción de línea de comandos **modificada** , debe especificar el nombre de los archivos de salida con las opciones **-MFL** y **-MOF** en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="8886b-119">If you use either the pragma amendment command or the **Amended** command-line option, you must specify the name of the output files using the **-MFL** and **-MOF** options at the command prompt.</span></span>

> [!Note]  
> <span data-ttu-id="8886b-120">El archivo MOF independiente del lenguaje que genera el compilador MOF contiene el equivalente decimal del ID. de configuración regional, aunque este valor se haya escrito en hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="8886b-120">The language-neutral MOF file that the MOF compiler generates contains the decimal equivalent of the locale ID, even if this value was entered in hexadecimal.</span></span> <span data-ttu-id="8886b-121">En el ejemplo anterior, el compilador ha convertido el valor 0xC0A al número decimal 1033 para el archivo de salida Lnmof. mof.</span><span class="sxs-lookup"><span data-stu-id="8886b-121">In the example above, the compiler has converted the value 0x409 to the decimal number 1033 for the Lnmof.mof output file.</span></span>

 

 

 



