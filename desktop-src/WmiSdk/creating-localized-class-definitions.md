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
# <a name="creating-localized-class-definitions"></a>Crear definiciones de clase localizadas

La creación de definiciones de clase localizadas es un proceso de tres pasos. Empiece por escribir el código MOF que define las clases, incluidos todos los calificadores que se deben localizar. Este archivo original se denomina el archivo "MOF maestro" porque contiene todos los calificadores y propiedades que definen la clase.

A continuación, utilice el [compilador MOF](mofcomp.md) para crear versiones independientes del idioma y específicas del idioma del archivo MOF. El compilador MOF coloca la descripción de la clase básica en un nuevo archivo MOF y crea una versión localizada del archivo MOF que solo contiene las propiedades y los calificadores que se deben localizar. Aunque las versiones específicas del idioma y del idioma del archivo MOF pueden tener el mismo nombre de archivo, debe utilizar una extensión de nombre de archivo. MFL para indicar que el archivo contiene información localizada. Puede localizar el archivo. MFL en otras configuraciones regionales, si es necesario. Almacenar las definiciones de clase en el repositorio CIM requiere un paso adicional del uso del compilador MOF para compilar los archivos MOF independientes del idioma y del idioma.

En los pasos siguientes se describe cómo crear y almacenar una definición de clase localizada.

**Para crear y almacenar una definición de clase localizada**

1.  Cree el archivo MOF maestro que define las clases que desea localizar.

    Guarde este código MOF en un archivo denominado Mastermof. mof.

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

2.  Cree versiones independientes del idioma y específicas del idioma del archivo MOF compilando el archivo MasterMOF. mof.

    Escriba el siguiente comando en un símbolo del sistema para compilar el archivo MasterMOF. mof.

    **MOFCOMP-MOF: Lnmof. mof-MFL: Lsmof. MFL-enmienda: MS \_ 409 Mastermof. mof**

3.  Compile los archivos independientes del idioma (Lnmof. mof) y específicos del idioma (Lsmof. MFL) y almacene la información de la clase en el repositorio CIM.

    Escriba los siguientes comandos en un símbolo del sistema para almacenar la información de clase en el repositorio CIM.

    **MOFCOMP Lnmof. mof**

    **MOFCOMP Lsmof. MFL**

    Después de compilar estos archivos, tendrá una definición de clase independiente del lenguaje en el \\ espacio de nombres de prueba raíz y una definición de clase localizada en el \\ espacio de \\ nombres MS 409 de prueba raíz \_ . Para obtener más información acerca de la compilación de archivos MOF localizados, consulte [compilar archivos MOF localizados](compiling-localized-mof-files.md).

 

 



