---
description: La creación de definiciones de clase localizadas es un proceso de tres pasos.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Crear definiciones de clase localizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717401"
---
# <a name="creating-localized-class-definitions"></a><span data-ttu-id="797fb-103">Crear definiciones de clase localizadas</span><span class="sxs-lookup"><span data-stu-id="797fb-103">Creating Localized Class Definitions</span></span>

<span data-ttu-id="797fb-104">La creación de definiciones de clase localizadas es un proceso de tres pasos.</span><span class="sxs-lookup"><span data-stu-id="797fb-104">Creating localized class definitions is a three-step process.</span></span> <span data-ttu-id="797fb-105">Empiece por escribir el código MOF que define las clases, incluidos todos los calificadores que se deben localizar.</span><span class="sxs-lookup"><span data-stu-id="797fb-105">You start by writing MOF code that defines the classes, including all qualifiers that must be localized.</span></span> <span data-ttu-id="797fb-106">Este archivo original se denomina el archivo "MOF maestro" porque contiene todos los calificadores y propiedades que definen la clase.</span><span class="sxs-lookup"><span data-stu-id="797fb-106">This original file is called the "master MOF" file because it contains all of the qualifiers and properties that define the class.</span></span>

<span data-ttu-id="797fb-107">A continuación, utilice el [compilador MOF](mofcomp.md) para crear versiones independientes del idioma y específicas del idioma del archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="797fb-107">Next, use the [MOF compiler](mofcomp.md) to create the language-neutral and language-specific versions of the MOF file.</span></span> <span data-ttu-id="797fb-108">El compilador MOF coloca la descripción de la clase básica en un nuevo archivo MOF y crea una versión localizada del archivo MOF que solo contiene las propiedades y los calificadores que se deben localizar.</span><span class="sxs-lookup"><span data-stu-id="797fb-108">The MOF compiler places the basic class description in a new MOF file and creates a localized version of the MOF file that contains only the properties and qualifiers that must be localized.</span></span> <span data-ttu-id="797fb-109">Aunque las versiones específicas del idioma y del idioma del archivo MOF pueden tener el mismo nombre de archivo, debe utilizar una extensión de nombre de archivo. MFL para indicar que el archivo contiene información localizada.</span><span class="sxs-lookup"><span data-stu-id="797fb-109">Although the language-specific and language-neutral versions of the MOF file can have the same file name, you should use a .mfl file name extension to indicate that the file contains localized information.</span></span> <span data-ttu-id="797fb-110">Puede localizar el archivo. MFL en otras configuraciones regionales, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="797fb-110">You can localize the .mfl file to other locales, if necessary.</span></span> <span data-ttu-id="797fb-111">Almacenar las definiciones de clase en el repositorio CIM requiere un paso adicional del uso del compilador MOF para compilar los archivos MOF independientes del idioma y del idioma.</span><span class="sxs-lookup"><span data-stu-id="797fb-111">Storing the class definitions in the CIM repository requires an additional step of using the MOF compiler to compile both the language-neutral and the language-specific MOF files.</span></span>

<span data-ttu-id="797fb-112">En los pasos siguientes se describe cómo crear y almacenar una definición de clase localizada.</span><span class="sxs-lookup"><span data-stu-id="797fb-112">The following steps describe how to create and store a localized class definition.</span></span>

<span data-ttu-id="797fb-113">**Para crear y almacenar una definición de clase localizada**</span><span class="sxs-lookup"><span data-stu-id="797fb-113">**To create and store a localized class definition**</span></span>

1.  <span data-ttu-id="797fb-114">Cree el archivo MOF maestro que define las clases que desea localizar.</span><span class="sxs-lookup"><span data-stu-id="797fb-114">Create the master MOF file that defines the classes that you want localized.</span></span>

    <span data-ttu-id="797fb-115">Guarde este código MOF en un archivo denominado Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="797fb-115">Save this MOF code in a file called Mastermof.mof.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  <span data-ttu-id="797fb-116">Cree versiones independientes del idioma y específicas del idioma del archivo MOF compilando el archivo MasterMOF. mof.</span><span class="sxs-lookup"><span data-stu-id="797fb-116">Create language-neutral and language-specific versions of the MOF file by compiling the MasterMOF.mof file.</span></span>

    <span data-ttu-id="797fb-117">Escriba el siguiente comando en un símbolo del sistema para compilar el archivo MasterMOF. mof.</span><span class="sxs-lookup"><span data-stu-id="797fb-117">Type the following command at a command prompt to compile the MasterMOF.mof file.</span></span>

    <span data-ttu-id="797fb-118">**MOFCOMP-MOF: Lnmof. mof-MFL: Lsmof. MFL-enmienda: MS \_ 409 Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="797fb-118">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

3.  <span data-ttu-id="797fb-119">Compile los archivos independientes del idioma (Lnmof. mof) y específicos del idioma (Lsmof. MFL) y almacene la información de la clase en el repositorio CIM.</span><span class="sxs-lookup"><span data-stu-id="797fb-119">Compile the language-neutral (Lnmof.mof) and language-specific (Lsmof.mfl) files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="797fb-120">Escriba los siguientes comandos en un símbolo del sistema para almacenar la información de clase en el repositorio CIM.</span><span class="sxs-lookup"><span data-stu-id="797fb-120">Type the following commands at a command prompt to store the class information in the CIM repository.</span></span>

    <span data-ttu-id="797fb-121">**MOFCOMP Lnmof. mof**</span><span class="sxs-lookup"><span data-stu-id="797fb-121">**Mofcomp Lnmof.mof**</span></span>

    <span data-ttu-id="797fb-122">**MOFCOMP Lsmof. MFL**</span><span class="sxs-lookup"><span data-stu-id="797fb-122">**Mofcomp Lsmof.mfl**</span></span>

    <span data-ttu-id="797fb-123">Después de compilar estos archivos, tendrá una definición de clase independiente del lenguaje en el \\ espacio de nombres de prueba raíz y una definición de clase localizada en el \\ espacio de \\ nombres MS 409 de prueba raíz \_ .</span><span class="sxs-lookup"><span data-stu-id="797fb-123">After you compile these files, you will have a language-neutral class definition in the root\\test namespace and a localized class definition in the root\\test\\ms\_409 namespace.</span></span> <span data-ttu-id="797fb-124">Para obtener más información acerca de la compilación de archivos MOF localizados, consulte [compilar archivos MOF localizados](compiling-localized-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="797fb-124">For more information about compiling localized MOF files, see [Compiling Localized MOF files](compiling-localized-mof-files.md).</span></span>

 

 



